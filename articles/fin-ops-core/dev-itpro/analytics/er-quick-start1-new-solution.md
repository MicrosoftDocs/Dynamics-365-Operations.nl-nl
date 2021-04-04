---
title: Een nieuwe ER-oplossing ontwerpen om een aangepast rapport af te drukken
description: In dit onderwerp wordt uitgelegd hoe u een oplossing voor elektronische rapportering (ER) kunt ontwerpen om een aangepast rapport af te drukken.
author: NickSelin
manager: AnnBe
ms.date: 08/10/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5bbfae36fb15437f2baadc66663cbfdb28691e8
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5562606"
---
# <a name="design-a-new-er-solution-to-print-a-custom-report"></a><span data-ttu-id="b79c2-103">Een nieuwe ER-oplossing ontwerpen om een aangepast rapport af te drukken</span><span class="sxs-lookup"><span data-stu-id="b79c2-103">Design a new ER solution to print a custom report</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b79c2-104">In de volgende stappen wordt uitgelegd hoe een gebruiker in de rol van systeembeheerder, ER-ontwikkelaar of ER-consultant parameters van het ER-raamwerk kan configureren, de vereiste nieuwe configuraties van een nieuwe ER-oplossing kan ontwerpen om toegang te krijgen tot de gegevens van een bepaald bedrijfsdomein en een aangepast rapport in de Microsoft Office-indeling kan genereren.</span><span class="sxs-lookup"><span data-stu-id="b79c2-104">The following steps explain how a user in the System Administrator, Electronic Reporting Developer, or Electronic Reporting Functional Consultant role can configure parameters of the ER framework, design the required ER configurations of a new ER solution to access the data of a particular business domain, and generate a custom report in Microsoft Office format.</span></span> <span data-ttu-id="b79c2-105">Deze stappen kunnen in het **USMF**-bedrijf worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="b79c2-105">These steps can be completed in the **USMF** company.</span></span>

- [<span data-ttu-id="b79c2-106">Het ER-raamwerk configureren</span><span class="sxs-lookup"><span data-stu-id="b79c2-106">Configure the ER framework</span></span>](#ConfigureFramework)

    - [<span data-ttu-id="b79c2-107">ER-parameters configureren</span><span class="sxs-lookup"><span data-stu-id="b79c2-107">Configure ER parameters</span></span>](#ConfigureParameters)
    - [<span data-ttu-id="b79c2-108">Een ER-configuratieprovider activeren</span><span class="sxs-lookup"><span data-stu-id="b79c2-108">Activate an ER configuration provider</span></span>](#ActivateProvider)

        - [<span data-ttu-id="b79c2-109">De lijst met ER-configuratie providers bekijken</span><span class="sxs-lookup"><span data-stu-id="b79c2-109">Review the list of ER configuration providers</span></span>](#ReviewProvidersList)
        - [<span data-ttu-id="b79c2-110">Een nieuwe ER-configuratieprovider toevoegen</span><span class="sxs-lookup"><span data-stu-id="b79c2-110">Add a new ER configuration provider</span></span>](#AddProvider)
        - [<span data-ttu-id="b79c2-111">Een ER-configuratieprovider activeren</span><span class="sxs-lookup"><span data-stu-id="b79c2-111">Activate an ER configuration provider</span></span>](#ActivateAddedProvider)

- [<span data-ttu-id="b79c2-112">Domeinspecifiek gegevensmodel ontwerpen</span><span class="sxs-lookup"><span data-stu-id="b79c2-112">Design a domain-specific data model</span></span>](#DesignModel)

    - [<span data-ttu-id="b79c2-113">Een nieuwe gegevensmodelconfiguratie importeren</span><span class="sxs-lookup"><span data-stu-id="b79c2-113">Import a new data model configuration</span></span>](#ImportDataModel)
    - [<span data-ttu-id="b79c2-114">Een nieuwe gegevensmodelconfiguratie maken</span><span class="sxs-lookup"><span data-stu-id="b79c2-114">Create a new data model configuration</span></span>](#DesignDataModel)

        - [<span data-ttu-id="b79c2-115">Het gegevensmodel een naam geven</span><span class="sxs-lookup"><span data-stu-id="b79c2-115">Name the data model</span></span>](#NameDataModel)
        - [<span data-ttu-id="b79c2-116">Gegevensmodelvelden toevoegen</span><span class="sxs-lookup"><span data-stu-id="b79c2-116">Add data model fields</span></span>](#FieldsEntry)
        - [<span data-ttu-id="b79c2-117">Het ontwerp van het gegevensmodel voltooien</span><span class="sxs-lookup"><span data-stu-id="b79c2-117">Complete the design of the data model</span></span>](#CompleteDataModel)

- [<span data-ttu-id="b79c2-118">Een modeltoewijzing voor het geconfigureerde gegevensmodel ontwerpen</span><span class="sxs-lookup"><span data-stu-id="b79c2-118">Design a model mapping for the configured data model</span></span>](#DesignMapping)

    - [<span data-ttu-id="b79c2-119">Een nieuwe configuratie voor de modeltoewijzing importeren</span><span class="sxs-lookup"><span data-stu-id="b79c2-119">Import a new model mapping configuration</span></span>](#ImportModelMapping)
    - [<span data-ttu-id="b79c2-120">Een nieuwe configuratie voor de modeltoewijzing maken</span><span class="sxs-lookup"><span data-stu-id="b79c2-120">Create a new model mapping configuration</span></span>](#CreateModelMapping)

        - [<span data-ttu-id="b79c2-121">Een nieuw modeltoewijzingsonderdeel ontwerpen</span><span class="sxs-lookup"><span data-stu-id="b79c2-121">Design a new model mapping component</span></span>](#DesignMappingComponent)
        - [<span data-ttu-id="b79c2-122">Gegevensbronnen toevoegen voor toegang tot toepassingstabellen</span><span class="sxs-lookup"><span data-stu-id="b79c2-122">Add data sources to access application tables</span></span>](#AddMmDataSource1)
        - [<span data-ttu-id="b79c2-123">Gegevensbronnen toevoegen voor toegang tot toepassingsopsommingen</span><span class="sxs-lookup"><span data-stu-id="b79c2-123">Add data sources to access application enumerations</span></span>](#AddMmDataSource2)
        - [<span data-ttu-id="b79c2-124">ER-labels toevoegen om een rapport in een opgegeven taal te genereren</span><span class="sxs-lookup"><span data-stu-id="b79c2-124">Add ER labels to generate a report in a specified language</span></span>](#AddMmLabels)
        - [<span data-ttu-id="b79c2-125">Een gegevensbron toevoegen om de resultaten van het vergelijken van opsommingswaarden met een tekstwaarde te transformeren</span><span class="sxs-lookup"><span data-stu-id="b79c2-125">Add a data source to transform the results of comparing enumeration values to a text value</span></span>](#AddMmDataSource3)
        - [<span data-ttu-id="b79c2-126">Gegevensbronnen binden aan gegevensmodelvelden</span><span class="sxs-lookup"><span data-stu-id="b79c2-126">Bind data sources to data model fields</span></span>](#AddMmBindings1)
        - [<span data-ttu-id="b79c2-127">Het ontwerp van de modeltoewijzing voltooien</span><span class="sxs-lookup"><span data-stu-id="b79c2-127">Complete the design of the model mapping</span></span>](#CompleteModelMapping)

- [<span data-ttu-id="b79c2-128">Een sjabloon voor een aangepast rapport ontwerpen</span><span class="sxs-lookup"><span data-stu-id="b79c2-128">Design a template for a custom report</span></span>](#DesignReportTemplate)
- [<span data-ttu-id="b79c2-129">Een indeling ontwerpen</span><span class="sxs-lookup"><span data-stu-id="b79c2-129">Design a format</span></span>](#DesignFormat)

    - [<span data-ttu-id="b79c2-130">Een ontworpen indelingsconfiguratie importeren</span><span class="sxs-lookup"><span data-stu-id="b79c2-130">Import a designed format configuration</span></span>](#FormatImport)
    - [<span data-ttu-id="b79c2-131">Een nieuwe indelingsconfiguratie maken</span><span class="sxs-lookup"><span data-stu-id="b79c2-131">Create a new format configuration</span></span>](#FormatCreate)

        - [<span data-ttu-id="b79c2-132">Een rapportsjabloon importeren</span><span class="sxs-lookup"><span data-stu-id="b79c2-132">Import a report template</span></span>](#ImportReportTemplate)
        - [<span data-ttu-id="b79c2-133">Een indeling configureren</span><span class="sxs-lookup"><span data-stu-id="b79c2-133">Configure a format</span></span>](#ConfigureFormat)
        - [<span data-ttu-id="b79c2-134">De gegevensbinding voor een rapporttitel definiëren</span><span class="sxs-lookup"><span data-stu-id="b79c2-134">Define the data binding for a report title</span></span>](#DefineFormatBindings)
        - [<span data-ttu-id="b79c2-135">De gegevensbron van het model controleren</span><span class="sxs-lookup"><span data-stu-id="b79c2-135">Review the model data source</span></span>](#ReviewModelDataSource)
        - [<span data-ttu-id="b79c2-136">Indelingselementen aan een gegevensbronvelden binden</span><span class="sxs-lookup"><span data-stu-id="b79c2-136">Bind format elements to data source fields</span></span>](#BindFormatElements)

    - [<span data-ttu-id="b79c2-137">Een ontwerpindeling vanuit ER uitvoeren</span><span class="sxs-lookup"><span data-stu-id="b79c2-137">Run a designed format from ER</span></span>](#RunFormatFromER)

- [<span data-ttu-id="b79c2-138">Een ontworpen indeling optimaliseren</span><span class="sxs-lookup"><span data-stu-id="b79c2-138">Tune a designed format</span></span>](#TuneFormat)

    - [<span data-ttu-id="b79c2-139">Een opmaak wijzigen om de naam van een gegenereerd document te veranderen</span><span class="sxs-lookup"><span data-stu-id="b79c2-139">Modify a format to change the name of a generated document</span></span>](#ModifyToChangeName)
    - [<span data-ttu-id="b79c2-140">Een opmaak wijzigen om de volgorde van vragen te veranderen</span><span class="sxs-lookup"><span data-stu-id="b79c2-140">Modify a format to change the order of questions</span></span>](#ModifyToOrder)
    - [<span data-ttu-id="b79c2-141">Een gewijzigde indeling vanuit ER uitvoeren</span><span class="sxs-lookup"><span data-stu-id="b79c2-141">Run a modified format from ER</span></span>](#RunFormatFromER2)
    - [<span data-ttu-id="b79c2-142">Het indelingsontwerp voltooien</span><span class="sxs-lookup"><span data-stu-id="b79c2-142">Complete the format design</span></span>](#CompleteFormat)

- [<span data-ttu-id="b79c2-143">Toepassingsartefacten ontwikkelen om het ontworpen rapport aan te roepen</span><span class="sxs-lookup"><span data-stu-id="b79c2-143">Develop application artefacts to call the designed report</span></span>](#DevelopCustomCode)

    - [<span data-ttu-id="b79c2-144">Broncode wijzigen</span><span class="sxs-lookup"><span data-stu-id="b79c2-144">Modify source code</span></span>](#ModifySourceCode)

        - [<span data-ttu-id="b79c2-145">Een gegevenscontractklasse toevoegen</span><span class="sxs-lookup"><span data-stu-id="b79c2-145">Add a data contract class</span></span>](#DataContractClass)
        - [<span data-ttu-id="b79c2-146">Een UI Builder-klasse toevoegen</span><span class="sxs-lookup"><span data-stu-id="b79c2-146">Add a UI builder class</span></span>](#UIBuilderClass)
        - [<span data-ttu-id="b79c2-147">Een gegevensproviderklasse toevoegen</span><span class="sxs-lookup"><span data-stu-id="b79c2-147">Add a data provider class</span></span>](#DataProviderClass)
        - [<span data-ttu-id="b79c2-148">Een labelbestand toevoegen</span><span class="sxs-lookup"><span data-stu-id="b79c2-148">Add a labels file</span></span>](#LabelsFile)
        - [<span data-ttu-id="b79c2-149">Een serviceklasse voor een rapport toevoegen</span><span class="sxs-lookup"><span data-stu-id="b79c2-149">Add a report service class</span></span>](#ServiceClass)
        - [<span data-ttu-id="b79c2-150">Een controllerklasse voor een rapport toevoegen</span><span class="sxs-lookup"><span data-stu-id="b79c2-150">Add a report controller class</span></span>](#ControllerClass)
        - [<span data-ttu-id="b79c2-151">Een menuopdracht toevoegen</span><span class="sxs-lookup"><span data-stu-id="b79c2-151">Add a menu item</span></span>](#MenuItem)
        - [<span data-ttu-id="b79c2-152">Een menuopdracht aan een menu toevoegen</span><span class="sxs-lookup"><span data-stu-id="b79c2-152">Add a menu item to a menu</span></span>](#Menu)
        - [<span data-ttu-id="b79c2-153">Een Visual Studio-project opbouwen</span><span class="sxs-lookup"><span data-stu-id="b79c2-153">Build a Visual Studio project</span></span>](#BuildVSProject)

    - [<span data-ttu-id="b79c2-154">Een indeling uit de toepassing uitvoeren</span><span class="sxs-lookup"><span data-stu-id="b79c2-154">Run a format from the application</span></span>](#RunFormatFromApp)

- [<span data-ttu-id="b79c2-155">Een ontworpen ER-oplossing optimaliseren</span><span class="sxs-lookup"><span data-stu-id="b79c2-155">Tune a designed ER solution</span></span>](#TuneSolution)

    - [<span data-ttu-id="b79c2-156">Een modeltoewijzing wijzigen</span><span class="sxs-lookup"><span data-stu-id="b79c2-156">Modify a model mapping</span></span>](#ModifyModelMapping)

        - [<span data-ttu-id="b79c2-157">Gegevensbronnen toevoegen voor toegang tot een gegevenscontractobject</span><span class="sxs-lookup"><span data-stu-id="b79c2-157">Add data sources to access a data contract object</span></span>](#AddDataSource1)
        - [<span data-ttu-id="b79c2-158">Een gegevensbron toevoegen voor toegang tot toewijzingsrecords met een ER-indeling</span><span class="sxs-lookup"><span data-stu-id="b79c2-158">Add a data source to access ER format mapping records</span></span>](#AddDataSource2)
        - [<span data-ttu-id="b79c2-159">Een gegevensbron toevoegen voor toegang tot indelingstoewijzingsrecord van een actieve ER-indeling</span><span class="sxs-lookup"><span data-stu-id="b79c2-159">Add a data source to access a format mapping record of a running ER format</span></span>](#AddDataSource3)
        - [<span data-ttu-id="b79c2-160">De naam van de actieve ER-indeling in het gegevensmodel invoeren</span><span class="sxs-lookup"><span data-stu-id="b79c2-160">Enter the name of the running ER format in the data model</span></span>](#AddBinding)
        - [<span data-ttu-id="b79c2-161">Het ontwerp van de modeltoewijzing voltooien</span><span class="sxs-lookup"><span data-stu-id="b79c2-161">Complete the design of the model mapping</span></span>](#CompleteModelMapping2)

    - [<span data-ttu-id="b79c2-162">Een indeling wijzigen</span><span class="sxs-lookup"><span data-stu-id="b79c2-162">Modify a format</span></span>](#ModifyFormat)

        - [<span data-ttu-id="b79c2-163">Een nieuw opmaakelement toevoegen</span><span class="sxs-lookup"><span data-stu-id="b79c2-163">Add a new format element</span></span>](#AddFormatElement)
        - [<span data-ttu-id="b79c2-164">Het toegevoegde indelingselement binden</span><span class="sxs-lookup"><span data-stu-id="b79c2-164">Bind the added format element</span></span>](#BindAddedFormatElement)
        - [<span data-ttu-id="b79c2-165">Het indelingsontwerp voltooien</span><span class="sxs-lookup"><span data-stu-id="b79c2-165">Complete the format design</span></span>](#CompleteFormat2)

    - [<span data-ttu-id="b79c2-166">Een indeling uit de toepassing uitvoeren</span><span class="sxs-lookup"><span data-stu-id="b79c2-166">Run a format from the application</span></span>](#RunFormatFromApp2)
    - [<span data-ttu-id="b79c2-167">Een indeling vanuit ER uitvoeren</span><span class="sxs-lookup"><span data-stu-id="b79c2-167">Run a format from ER</span></span>](#RunFormatFromER3)
    - [<span data-ttu-id="b79c2-168">Een indelingsbestemming configureren voor voorvertoning op het scherm</span><span class="sxs-lookup"><span data-stu-id="b79c2-168">Configure a format destination for on-screen preview</span></span>](#ConfigureDestination)
    - [<span data-ttu-id="b79c2-169">Een indeling van de toepassing uitvoeren voor voorvertoning als PDF-document</span><span class="sxs-lookup"><span data-stu-id="b79c2-169">Run a format from the application to preview it as a PDF document</span></span>](#RunFormatFromApp3)

- [<span data-ttu-id="b79c2-170">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="b79c2-170">Additional resources</span></span>](#References)

<span data-ttu-id="b79c2-171">In dit voorbeeld maakt u een nieuwe ER-oplossing voor de module [Vragenlijst](https://docs.microsoft.com/dynamics365/human-resources/hr-learning-questionnaires).</span><span class="sxs-lookup"><span data-stu-id="b79c2-171">In this example, you will create a new ER solution for the [Questionnaire](https://docs.microsoft.com/dynamics365/human-resources/hr-learning-questionnaires) module.</span></span> <span data-ttu-id="b79c2-172">Met deze nieuwe ER-oplossing kunt u een rapport ontwerpen met een Microsoft Excel-werkblad als sjabloon.</span><span class="sxs-lookup"><span data-stu-id="b79c2-172">This new ER solution lets you design a report by using a Microsoft Excel worksheet as a template.</span></span> <span data-ttu-id="b79c2-173">U kunt het rapport **Vragenlijst** vervolgens genereren in Excel- of PDF-indeling, naast het bestaande SSRS-rapport (SQL Server Reporting Services).</span><span class="sxs-lookup"><span data-stu-id="b79c2-173">You can then generate the **Questionnaire** report in Excel or PDF format, in addition to generating the existing SQL Server Reporting Services (SSRS) report.</span></span> <span data-ttu-id="b79c2-174">U kunt het nieuwe rapport ook later wijzigen op verzoek.</span><span class="sxs-lookup"><span data-stu-id="b79c2-174">You can also modify the new report later, upon request.</span></span> <span data-ttu-id="b79c2-175">U hoeft hiervoor geen code te schrijven.</span><span class="sxs-lookup"><span data-stu-id="b79c2-175">No coding is required.</span></span>

1. <span data-ttu-id="b79c2-176">Als u het bestaande rapport wilt uitvoeren, gaat u naar **Vragenlijst** \> **Ontwerpen** \> **Rapport vragenlijsten**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-176">To run the existing report, go to **Questionnaire** \> **Design** \> **Questionnaires report**.</span></span>

    ![Het menu-item Rapport vragenlijsten selecteren in de module Vragenlijst om het bestaande SSRS-rapport uit te voeren](./media/er-quick-start1-application-menu-origin.png)

2. <span data-ttu-id="b79c2-178">Geef selectiecriteria op in het dialoogvenster **Rapport vragenlijsten**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-178">In the **Questionnaires report** dialog box, specify selection criteria.</span></span> <span data-ttu-id="b79c2-179">Pas een filter toe zodat het rapport alleen de vragenlijst **SBCCrsExam** bevat.</span><span class="sxs-lookup"><span data-stu-id="b79c2-179">Apply a filter so that the report includes only the **SBCCrsExam** questionnaire.</span></span>

    ![Selectiecriteria opgeven in het dialoogvenster Rapport vragenlijsten](./media/er-quick-start1-ssrs-report-dialog.png)

<span data-ttu-id="b79c2-181">In de volgende afbeelding ziet u de gegenereerde versie van het SSRS-rapport voor de vragenlijst **SBCCrsExam**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-181">The following illustration shows the generated version of the SSRS report for the **SBCCrsExam** questionnaire.</span></span>

![Gegenereerd SSRS-rapport](./media/er-quick-start1-ssrs-report.png)

## <a name="configure-the-er-framework"></a><a name="ConfigureFramework"></a><span data-ttu-id="b79c2-183">Het ER-raamwerk configureren</span><span class="sxs-lookup"><span data-stu-id="b79c2-183">Configure the ER framework</span></span>

<span data-ttu-id="b79c2-184">Als u een gebruiker bent in de rol ER-ontwikkelaar, moet u de minimale set ER-parameters configureren voordat u het ER-framework kunt gaan gebruiken om een nieuwe ER-oplossing te ontwerpen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-184">As a user in the Electronic Reporting Developer role, you must configure the minimal set of ER parameters before you can start to use the ER framework to design your new ER solution.</span></span>

### <a name="configure-er-parameters"></a><a name="ConfigureParameters"></a><span data-ttu-id="b79c2-185">ER-parameters configureren</span><span class="sxs-lookup"><span data-stu-id="b79c2-185">Configure ER parameters</span></span>

1. <span data-ttu-id="b79c2-186">Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-186">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="b79c2-187">Selecteer in de werkruimte **Elektronische rapportage** **Parameters van elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-187">In the **Electronic reporting** workspace, select **Electronic reporting parameters**.</span></span>
3. <span data-ttu-id="b79c2-188">Stel op de pagina **Parameters van elektronische rapportage** op het tabblad **Algemeen** de optie **Ontwerpmodus inschakelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-188">On the **Electronic reporting parameters** page, on the **General** tab, set the **Enable design mode** option to **Yes**.</span></span>
4. <span data-ttu-id="b79c2-189">Stel op het tabblad **Bijlagen** de volgende parameters in:</span><span class="sxs-lookup"><span data-stu-id="b79c2-189">On the **Attachments** tab, set the following parameters:</span></span>

    - <span data-ttu-id="b79c2-190">Stel het veld **Configuraties** in op **Bestand** voor het bedrijf **USMF**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-190">Set the **Configurations** field to **File** for the **USMF** company.</span></span>
    - <span data-ttu-id="b79c2-191">Stel de velden **Taakarchief**, **Tijdelijk**, **Basislijn** en **Overige** in op **Bestand**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-191">Set **Job archive**, **Temporary**, **Baseline**, and **Others** fields to **File**.</span></span>

<span data-ttu-id="b79c2-192">Meer informatie over het configureren van ER-parameters vindt u in [Het ER-raamwerk configureren](electronic-reporting-er-configure-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="b79c2-192">For more information about ER parameters, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md).</span></span>

### <a name="activate-an-er-configuration-provider"></a><a name="ActivateProvider"></a><span data-ttu-id="b79c2-193">Een ER-configuratieprovider activeren</span><span class="sxs-lookup"><span data-stu-id="b79c2-193">Activate an ER configuration provider</span></span>

<span data-ttu-id="b79c2-194">Elke ER-configuratie wordt gemarkeerd als het eigendom van een ER-configuratieprovider.</span><span class="sxs-lookup"><span data-stu-id="b79c2-194">Every ER configuration is marked as owned by an ER configuration provider.</span></span> <span data-ttu-id="b79c2-195">Daarom moet u een ER-configuratieprovider activeren in de werkruimte **Elektronische rapportage** voordat u een ER-configuratie gaat toevoegen of bewerken.</span><span class="sxs-lookup"><span data-stu-id="b79c2-195">Therefore, you must activate an ER configuration provider in the **Electronic reporting** workspace before you start to add or edit any ER configurations.</span></span>

> [!NOTE]
> <span data-ttu-id="b79c2-196">Alleen de eigenaar van een ER-configuratie kan deze bewerken.</span><span class="sxs-lookup"><span data-stu-id="b79c2-196">Only the owner of an ER configuration can edit it.</span></span> <span data-ttu-id="b79c2-197">Daarom moet een geschikte ER-configuratieprovider worden geactiveerd in de werkruimte **Elektronische rapportage**, voordat een ER-configuratie kan worden bewerkt.</span><span class="sxs-lookup"><span data-stu-id="b79c2-197">Therefore, before an ER configuration can be edited, the appropriate ER configuration provider must be activated in the **Electronic reporting** workspace.</span></span>

#### <a name="review-the-list-of-er-configuration-providers"></a><a name="ReviewProvidersList"></a><span data-ttu-id="b79c2-198">De lijst met ER-configuratie providers bekijken</span><span class="sxs-lookup"><span data-stu-id="b79c2-198">Review the list of ER configuration providers</span></span>

1. <span data-ttu-id="b79c2-199">Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-199">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="b79c2-200">Selecteer in het werkgebied **Elektronische rapportage** in de sectie **Verwante koppelingen** de optie **Configuratieproviders**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-200">In the **Electronic reporting** workspace, in the **Related links** section, select **Configuration providers**.</span></span>
3. <span data-ttu-id="b79c2-201">Op de pagina **Configuratieproviders** heeft elke providerrecord een unieke naam en een unieke URL.</span><span class="sxs-lookup"><span data-stu-id="b79c2-201">On the **Configuration providers** page, each configuration provider record has a unique name and URL.</span></span> <span data-ttu-id="b79c2-202">Bekijk de inhoud van deze pagina.</span><span class="sxs-lookup"><span data-stu-id="b79c2-202">Review the contents of this page.</span></span> <span data-ttu-id="b79c2-203">Als er al een record bestaat voor **Litware, Inc.** (`https://www.litware.com`), kunt u de volgende procedure, [Een nieuwe ER-configuratieprovider toevoegen](#ActivateProvider), overslaan.</span><span class="sxs-lookup"><span data-stu-id="b79c2-203">If a record for **Litware, Inc.** (`https://www.litware.com`) already exists, skip the next procedure, [Add a new ER configuration provider](#ActivateProvider).</span></span>

#### <a name="add-a-new-er-configuration-provider"></a><a name="AddProvider"></a><span data-ttu-id="b79c2-204">Een nieuwe ER-configuratieprovider toevoegen</span><span class="sxs-lookup"><span data-stu-id="b79c2-204">Add a new ER configuration provider</span></span>

1. <span data-ttu-id="b79c2-205">Selecteer **Nieuw** op de pagina **Configuratieproviders**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-205">On the **Configuration providers** page, select **New**.</span></span>
2. <span data-ttu-id="b79c2-206">Voer in het veld **Naam** de tekst **Litware, Inc.** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-206">In the **Name** field, enter **Litware, Inc.**</span></span>
3. <span data-ttu-id="b79c2-207">Voer in het veld **Internetadres** de tekst `https://www.litware.com` in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-207">In the **Internet address** field, enter `https://www.litware.com`.</span></span>
4. <span data-ttu-id="b79c2-208">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-208">Select **Save**.</span></span>

#### <a name="activate-an-er-configuration-provider"></a><a name="ActivateAddedProvider"></a><span data-ttu-id="b79c2-209">Een ER-configuratieprovider activeren</span><span class="sxs-lookup"><span data-stu-id="b79c2-209">Activate an ER configuration provider</span></span>

1. <span data-ttu-id="b79c2-210">Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-210">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="b79c2-211">Selecteer in het werkgebied **Elektronische rapportage** de configuratieprovider **Litware, Inc.**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-211">In the **Electronic reporting** workspace, select the **Litware, Inc.** configuration provider.</span></span>
3. <span data-ttu-id="b79c2-212">Selecteer **Instellingen als actief**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-212">Select **Set active**.</span></span>

<span data-ttu-id="b79c2-213">Meer informatie over ER-configuratieproviders vindt u in [Configuratieproviders maken en deze als actief markeren](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span><span class="sxs-lookup"><span data-stu-id="b79c2-213">For more information about ER configuration providers, see [Create configuration providers and mark them as active](tasks/er-configuration-provider-mark-it-active-2016-11.md).</span></span>

## <a name="design-a-domain-specific-data-model"></a><a name="DesignModel"></a><span data-ttu-id="b79c2-214">Domeinspecifiek gegevensmodel ontwerpen</span><span class="sxs-lookup"><span data-stu-id="b79c2-214">Design a domain-specific data model</span></span>

<span data-ttu-id="b79c2-215">U moet een nieuwe ER-configuratie maken die een onderdeel met een [gegevensmodel](general-electronic-reporting.md#data-model-and-model-mapping-components) bevat voor het bedrijfsdomein **Vragenlijst**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-215">You must create a new ER configuration that contains a [data model](general-electronic-reporting.md#data-model-and-model-mapping-components) component for the **Questionnaire** business domain.</span></span> <span data-ttu-id="b79c2-216">Dit gegevensmodel wordt later gebruikt als gegevensbron wanneer u een ER-indeling ontwerpt om het rapport **Vragenlijst** te genereren.</span><span class="sxs-lookup"><span data-stu-id="b79c2-216">This data model will later be used as a data source when you design an ER format to generate the **Questionnaire** report.</span></span>

<span data-ttu-id="b79c2-217">Door de stappen in de sectie [Een nieuwe gegevensmodelconfiguratie importeren](#ImportDataModel) te voltooien, kunt u het vereiste gegevensmodel importeren uit het opgegeven XML-bestand.</span><span class="sxs-lookup"><span data-stu-id="b79c2-217">By completing the steps in the [Import a new data model configuration](#ImportDataModel) section, you can import the required data model from the provided XML file.</span></span> <span data-ttu-id="b79c2-218">U kunt de stappen in de sectie [Een nieuwe gegevensmodelconfiguratie maken](#DesignDataModel) ook uitvoeren als u een helemaal nieuw gegevensmodel wilt ontwerpen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-218">Alternatively, you can complete the steps in the [Create a new data model configuration](#DesignDataModel) section to design this data model from scratch.</span></span>

### <a name="import-a-new-data-model-configuration"></a><a name="ImportDataModel"></a><span data-ttu-id="b79c2-219">Een nieuwe gegevensmodelconfiguratie importeren</span><span class="sxs-lookup"><span data-stu-id="b79c2-219">Import a new data model configuration</span></span>

1. <span data-ttu-id="b79c2-220">Download het bestand [Questionnaires model.version.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) en sla het op uw lokale computer op.</span><span class="sxs-lookup"><span data-stu-id="b79c2-220">Download the [Questionnaires model.version.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="b79c2-221">Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-221">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="b79c2-222">Selecteer in het werkgebied **Elektronische rapportage** de optie **Rapportconfiguraties**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-222">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="b79c2-223">In het actievenster selecteert u **Uitwisselen** \> **Laden uit XML-bestand**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-223">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="b79c2-224">Selecteer **Bladeren** en zoek en selecteer het bestand **Questionnaires model.version.1.xml**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-224">Select **Browse**, and then find and select the **Questionnaires model.version.1.xml** file.</span></span>
6. <span data-ttu-id="b79c2-225">Selecteer **OK** om de configuratie te importeren.</span><span class="sxs-lookup"><span data-stu-id="b79c2-225">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="b79c2-226">Als u wilt doorgaan, gaat u naar de volgende procedure [Een nieuwe gegevensmodelconfiguratie maken](#DesignDataModel).</span><span class="sxs-lookup"><span data-stu-id="b79c2-226">To continue, skip the next procedure, [Create a new data model configuration](#DesignDataModel).</span></span>

### <a name="create-a-new-data-model-configuration"></a><a name="DesignDataModel"></a><span data-ttu-id="b79c2-227">Een nieuwe gegevensmodelconfiguratie maken</span><span class="sxs-lookup"><span data-stu-id="b79c2-227">Create a new data model configuration</span></span>

1. <span data-ttu-id="b79c2-228">Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-228">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
2. <span data-ttu-id="b79c2-229">Selecteer in het werkgebied **Elektronische rapportage** de optie **Rapportconfiguraties**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-229">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
3. <span data-ttu-id="b79c2-230">Selecteer **Configuratie maken**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-230">Select **Create configuration**.</span></span>
4. <span data-ttu-id="b79c2-231">Voer in het vervolgkeuzemenu in het veld **Naam** **Vragenlijstmodel** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-231">In the drop-down dialog box, in the **Name** field, enter **Questionnaire model**.</span></span>
5. <span data-ttu-id="b79c2-232">Selecteer **Configuratie maken** om de configuratie te maken.</span><span class="sxs-lookup"><span data-stu-id="b79c2-232">Select **Create configuration** to create the configuration.</span></span>

#### <a name="name-the-data-model"></a><a name="NameDataModel"></a><span data-ttu-id="b79c2-233">Het gegevensmodel een naam geven</span><span class="sxs-lookup"><span data-stu-id="b79c2-233">Name the data model</span></span>

1. <span data-ttu-id="b79c2-234">Selecteer op de pagina **Configuraties** in de structuur met configuraties **Vragenlijstmodel**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-234">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
2. <span data-ttu-id="b79c2-235">Selecteer **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-235">Select **Designer**.</span></span>
3. <span data-ttu-id="b79c2-236">Voer op de pagina **Gegevensmodel ontwerpen** op het sneltabblad **Algemeen** in het veld **Naam** <a name="DataModeName"></a>**Vragenlijsten** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-236">On the **Data model designer** page, on the **General** FastTab, in the **Name** field, enter <a name="DataModeName"></a>**Questionnaires**.</span></span>

#### <a name="add-new-data-model-fields"></a><a name="FieldsEntry"></a><span data-ttu-id="b79c2-237">Nieuwe gegevensmodelvelden toevoegen</span><span class="sxs-lookup"><span data-stu-id="b79c2-237">Add new data model fields</span></span>

1. <span data-ttu-id="b79c2-238">Selecteer **Nieuw** op de pagina **Gegevensmodel ontwerpen**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-238">On the **Data model designer** page, select **New**.</span></span>
2. <span data-ttu-id="b79c2-239">Voer de volgende stappen uit in het vervolgkeuzemenu voor het toevoegen van een knooppunt voor een gegevensmodel:</span><span class="sxs-lookup"><span data-stu-id="b79c2-239">In the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="b79c2-240">Selecteer **Modelbasis** als type voor het nieuwe knooppunt.</span><span class="sxs-lookup"><span data-stu-id="b79c2-240">Select **Model root** as the type of the new node.</span></span>
    2. <span data-ttu-id="b79c2-241">Voer in het veld **Naam** <a name="RootDefinitionName"></a>**Basis** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-241">In the **Name** field, enter <a name="RootDefinitionName"></a>**Root**.</span></span>
    3. <span data-ttu-id="b79c2-242">Selecteer **Toevoegen** om het nieuwe knooppunt toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-242">Select **Add** to add the new node.</span></span>

    <span data-ttu-id="b79c2-243">Deze basisdescriptor wordt gebruikt om gegevens voor het rapport **Vragenlijst** te leveren.</span><span class="sxs-lookup"><span data-stu-id="b79c2-243">This root descriptor will be used to provide data for the **Questionnaire** report.</span></span> <span data-ttu-id="b79c2-244">Eén gegevensmodel kan meerdere descriptors hebben.</span><span class="sxs-lookup"><span data-stu-id="b79c2-244">A single data model can have multiple descriptors.</span></span> <span data-ttu-id="b79c2-245">Elke descriptor kan worden opgegeven voor één ER-indeling om gegevens te identificeren die nodig zijn om het rapport te genereren.</span><span class="sxs-lookup"><span data-stu-id="b79c2-245">Each descriptor can be specified for a single ER format, to identify data that is required to generate the report.</span></span>

3. <span data-ttu-id="b79c2-246">Selecteer nogmaals **Nieuw** en voer de volgende stappen uit in het vervolgkeuzemenu voor het toevoegen van een knooppunt voor een gegevensmodel:</span><span class="sxs-lookup"><span data-stu-id="b79c2-246">Select **New** again, and then, in the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="b79c2-247">Selecteer **Onderliggende waarde van een actief knooppunt** als het type van het nieuwe knooppunt.</span><span class="sxs-lookup"><span data-stu-id="b79c2-247">Select **Child of an active node** as the type of the new node.</span></span>
    2. <span data-ttu-id="b79c2-248">Voer in het veld **Naam** **BedrijfsNaam** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-248">In the **Name** field, enter **CompanyName**.</span></span>
    3. <span data-ttu-id="b79c2-249">Selecteer in het veld **Itemtype** **Tekenreeks**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-249">In the **Item type** field, select **String**.</span></span>
    4. <span data-ttu-id="b79c2-250">Selecteer **Toevoegen** om het nieuwe veld toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-250">Select **Add** to add the new field.</span></span>

    <span data-ttu-id="b79c2-251">Dit veld is vereist om de naam van het huidige bedrijf door te geven aan een ER-rapport waarin dit gegevensmodel wordt gebruikt als gegevensbron.</span><span class="sxs-lookup"><span data-stu-id="b79c2-251">This field is required to pass the name of the current company to an ER report that consumes this data model as a data source.</span></span>

4. <span data-ttu-id="b79c2-252">Selecteer nogmaals **Nieuw** en voer de volgende stappen uit in het vervolgkeuzemenu voor het toevoegen van een knooppunt voor een gegevensmodel:</span><span class="sxs-lookup"><span data-stu-id="b79c2-252">Select **New** again, and then, in the drop-down dialog box for adding a data model node, follow these steps:</span></span>

    1. <span data-ttu-id="b79c2-253">Selecteer **Onderliggende waarde van een actief knooppunt** als het type van het nieuwe knooppunt.</span><span class="sxs-lookup"><span data-stu-id="b79c2-253">Select **Child of an active node** as the type of the new node.</span></span>
    2. <span data-ttu-id="b79c2-254">Voer in het veld **Naam** **Vragenlijst** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-254">In the **Name** field, enter **Questionnaire**.</span></span>
    3. <span data-ttu-id="b79c2-255">Selecteer in het veld **Itemtype** **Recordlijst**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-255">In the **Item type** field, select **Record list**.</span></span>
    4. <span data-ttu-id="b79c2-256">Selecteer **Toevoegen** om het nieuwe veld toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-256">Select **Add** to add the new field.</span></span>

    <span data-ttu-id="b79c2-257">Dit veld is vereist om de lijst met vragenlijsten door te geven aan een ER-rapport waarin dit gegevensmodel wordt gebruikt als gegevensbron.</span><span class="sxs-lookup"><span data-stu-id="b79c2-257">This field will be used to pass the list of questionnaires to an ER report that consumes this data model as a data source.</span></span>

5. <span data-ttu-id="b79c2-258">Selecteer het knooppunt **Vragenlijst**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-258">Select the **Questionnaire** node.</span></span>
6. <span data-ttu-id="b79c2-259">Voeg de vereiste velden van het bewerkbare gegevensmodel op dezelfde manier toe totdat u de volgende gegevensmodelstructuur hebt voltooid.</span><span class="sxs-lookup"><span data-stu-id="b79c2-259">Continue to add the required fields of the editable data model in the same manner until you complete the following data model structure.</span></span>

    | <span data-ttu-id="b79c2-260">Veldpad</span><span class="sxs-lookup"><span data-stu-id="b79c2-260">Field path</span></span>                                                    | <span data-ttu-id="b79c2-261">Gegevenstype</span><span class="sxs-lookup"><span data-stu-id="b79c2-261">Data type</span></span>   | <span data-ttu-id="b79c2-262">Veldtoewijzing/geretourneerde waarde</span><span class="sxs-lookup"><span data-stu-id="b79c2-262">Field designation/returned value</span></span> |
    |---------------------------------------------------------------|-------------|----------------------------------|
    | <span data-ttu-id="b79c2-263">Hoofdmap</span><span class="sxs-lookup"><span data-stu-id="b79c2-263">Root</span></span>                                                          |             | <span data-ttu-id="b79c2-264">Het referentiepunt voor het aanvragen van vragenlijstgegevens.</span><span class="sxs-lookup"><span data-stu-id="b79c2-264">The reference point to request questionnaire data.</span></span> |
    | <span data-ttu-id="b79c2-265">Root\\CompanyName</span><span class="sxs-lookup"><span data-stu-id="b79c2-265">Root\\CompanyName</span></span>                                             | <span data-ttu-id="b79c2-266">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="b79c2-266">String</span></span>      | <span data-ttu-id="b79c2-267">De naam van het huidige bedrijf.</span><span class="sxs-lookup"><span data-stu-id="b79c2-267">The name of the current company.</span></span> |
    | <span data-ttu-id="b79c2-268">Root\\ExecutionContext</span><span class="sxs-lookup"><span data-stu-id="b79c2-268">Root\\ExecutionContext</span></span>                                        | <span data-ttu-id="b79c2-269">Registreren</span><span class="sxs-lookup"><span data-stu-id="b79c2-269">Record</span></span>      | <span data-ttu-id="b79c2-270">Details voor uitvoering van de indeling.</span><span class="sxs-lookup"><span data-stu-id="b79c2-270">Format execution details.</span></span> |
    | <span data-ttu-id="b79c2-271">Root\\ExecutionContext\\FormatName</span><span class="sxs-lookup"><span data-stu-id="b79c2-271">Root\\ExecutionContext\\FormatName</span></span>                            | <span data-ttu-id="b79c2-272">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="b79c2-272">String</span></span>      | <span data-ttu-id="b79c2-273">De naam van de ER-indeling die wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="b79c2-273">The name of the ER format that is being run.</span></span> |
    | <span data-ttu-id="b79c2-274">Root\\Questionnaire</span><span class="sxs-lookup"><span data-stu-id="b79c2-274">Root\\Questionnaire</span></span>                                           | <span data-ttu-id="b79c2-275">Recordlijst</span><span class="sxs-lookup"><span data-stu-id="b79c2-275">Record list</span></span> | <span data-ttu-id="b79c2-276">De lijst met vragenlijsten</span><span class="sxs-lookup"><span data-stu-id="b79c2-276">The list of questionnaires</span></span> |
    | <span data-ttu-id="b79c2-277">Root\\Questionnaire\\Active</span><span class="sxs-lookup"><span data-stu-id="b79c2-277">Root\\Questionnaire\\Active</span></span>                                   | <span data-ttu-id="b79c2-278">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="b79c2-278">String</span></span>      | <span data-ttu-id="b79c2-279">De status van de huidige vragenlijst.</span><span class="sxs-lookup"><span data-stu-id="b79c2-279">The status of the current questionnaire.</span></span> |
    | <span data-ttu-id="b79c2-280">Root\\Questionnaire\\Code</span><span class="sxs-lookup"><span data-stu-id="b79c2-280">Root\\Questionnaire\\Code</span></span>                                     | <span data-ttu-id="b79c2-281">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="b79c2-281">String</span></span>      | <span data-ttu-id="b79c2-282">De code van de huidige vragenlijst.</span><span class="sxs-lookup"><span data-stu-id="b79c2-282">The code of the current questionnaire.</span></span> |
    | <span data-ttu-id="b79c2-283">Root\\Questionnaire\\Description</span><span class="sxs-lookup"><span data-stu-id="b79c2-283">Root\\Questionnaire\\Description</span></span>                              | <span data-ttu-id="b79c2-284">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="b79c2-284">String</span></span>      | <span data-ttu-id="b79c2-285">De beschrijving van de huidige vragenlijst.</span><span class="sxs-lookup"><span data-stu-id="b79c2-285">The description of the current questionnaire.</span></span> |
    | <span data-ttu-id="b79c2-286">Root\\Questionnaire\\QuestionnaireType</span><span class="sxs-lookup"><span data-stu-id="b79c2-286">Root\\Questionnaire\\QuestionnaireType</span></span>                        | <span data-ttu-id="b79c2-287">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="b79c2-287">String</span></span>      | <span data-ttu-id="b79c2-288">Het type van de huidige vragenlijst.</span><span class="sxs-lookup"><span data-stu-id="b79c2-288">The type of the current questionnaire.</span></span> |
    | <span data-ttu-id="b79c2-289">Root\\Questionnaire\\QuestionOrder</span><span class="sxs-lookup"><span data-stu-id="b79c2-289">Root\\Questionnaire\\QuestionOrder</span></span>                            | <span data-ttu-id="b79c2-290">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="b79c2-290">String</span></span>      | <span data-ttu-id="b79c2-291">De numerieke volgorde van de huidige vragenlijst.</span><span class="sxs-lookup"><span data-stu-id="b79c2-291">The numerical order of the current questionnaire.</span></span> |
    | <span data-ttu-id="b79c2-292">Root\\Questionnaire\\ResultsGroup</span><span class="sxs-lookup"><span data-stu-id="b79c2-292">Root\\Questionnaire\\ResultsGroup</span></span>                             | <span data-ttu-id="b79c2-293">Registreren</span><span class="sxs-lookup"><span data-stu-id="b79c2-293">Record</span></span>      | <span data-ttu-id="b79c2-294">De resultaatparameters van de huidige vragenlijst.</span><span class="sxs-lookup"><span data-stu-id="b79c2-294">The result parameters of the current questionnaire.</span></span> |
    | <span data-ttu-id="b79c2-295">Root\\Questionnaire\\ResultsGroup\\Code</span><span class="sxs-lookup"><span data-stu-id="b79c2-295">Root\\Questionnaire\\ResultsGroup\\Code</span></span>                       | <span data-ttu-id="b79c2-296">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="b79c2-296">String</span></span>      | <span data-ttu-id="b79c2-297">De identificatiecode van de huidige resultaatgroep.</span><span class="sxs-lookup"><span data-stu-id="b79c2-297">The identification code of the current result group.</span></span> |
    | <span data-ttu-id="b79c2-298">Root\\Questionnaire\\ResultsGroup\\Description</span><span class="sxs-lookup"><span data-stu-id="b79c2-298">Root\\Questionnaire\\ResultsGroup\\Description</span></span>                | <span data-ttu-id="b79c2-299">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="b79c2-299">String</span></span>      | <span data-ttu-id="b79c2-300">De beschrijving van de huidige resultaatgroep.</span><span class="sxs-lookup"><span data-stu-id="b79c2-300">The description of the current result group.</span></span> |
    | <span data-ttu-id="b79c2-301">Root\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span><span class="sxs-lookup"><span data-stu-id="b79c2-301">Root\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>          | <span data-ttu-id="b79c2-302">Real-modus</span><span class="sxs-lookup"><span data-stu-id="b79c2-302">Real</span></span>        | <span data-ttu-id="b79c2-303">Het maximumaantal punten dat kan worden verdiend.</span><span class="sxs-lookup"><span data-stu-id="b79c2-303">The maximum number of points that could be earned.</span></span> |
    | <span data-ttu-id="b79c2-304">Root\\Questionnaire\\Question</span><span class="sxs-lookup"><span data-stu-id="b79c2-304">Root\\Questionnaire\\Question</span></span>                                 | <span data-ttu-id="b79c2-305">Recordlijst</span><span class="sxs-lookup"><span data-stu-id="b79c2-305">Record list</span></span> | <span data-ttu-id="b79c2-306">De lijst met vragen voor de huidige vragenlijst.</span><span class="sxs-lookup"><span data-stu-id="b79c2-306">The list of questions for the current questionnaire.</span></span> |
    | <span data-ttu-id="b79c2-307">Root\\Questionnaire\\Question\\CollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="b79c2-307">Root\\Questionnaire\\Question\\CollectionSequenceNumber</span></span>       | <span data-ttu-id="b79c2-308">Geheel getal</span><span class="sxs-lookup"><span data-stu-id="b79c2-308">Integer</span></span>     | <span data-ttu-id="b79c2-309">Het volgnummer van de huidige antwoordverzameling.</span><span class="sxs-lookup"><span data-stu-id="b79c2-309">The sequence number of the current answer collection.</span></span> |
    | <span data-ttu-id="b79c2-310">Root\\Questionnaire\\Question\\Id</span><span class="sxs-lookup"><span data-stu-id="b79c2-310">Root\\Questionnaire\\Question\\Id</span></span>                             | <span data-ttu-id="b79c2-311">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="b79c2-311">String</span></span>      | <span data-ttu-id="b79c2-312">De identificatiecode van de huidige vraag.</span><span class="sxs-lookup"><span data-stu-id="b79c2-312">The identification code of the current question.</span></span> |
    | <span data-ttu-id="b79c2-313">Root\\Questionnaire\\Question\\MustBeCompleted</span><span class="sxs-lookup"><span data-stu-id="b79c2-313">Root\\Questionnaire\\Question\\MustBeCompleted</span></span>                | <span data-ttu-id="b79c2-314">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="b79c2-314">String</span></span>      | <span data-ttu-id="b79c2-315">Een markering die aangeeft of de huidige vraag moet worden beantwoord.</span><span class="sxs-lookup"><span data-stu-id="b79c2-315">A flag that indicates whether the current question must be answered.</span></span> |
    | <span data-ttu-id="b79c2-316">Root\\Questionnaire\\Question\\PrimaryQuestion</span><span class="sxs-lookup"><span data-stu-id="b79c2-316">Root\\Questionnaire\\Question\\PrimaryQuestion</span></span>                | <span data-ttu-id="b79c2-317">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="b79c2-317">String</span></span>      | <span data-ttu-id="b79c2-318">Een markering die aangeeft of de huidige vraag primair is.</span><span class="sxs-lookup"><span data-stu-id="b79c2-318">A flag that indicates whether the current question is primary.</span></span> |
    | <span data-ttu-id="b79c2-319">Root\\Questionnaire\\Question\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="b79c2-319">Root\\Questionnaire\\Question\\SequenceNumber</span></span>                 | <span data-ttu-id="b79c2-320">Geheel getal</span><span class="sxs-lookup"><span data-stu-id="b79c2-320">Integer</span></span>     | <span data-ttu-id="b79c2-321">Het volgnummer van de huidige vraag.</span><span class="sxs-lookup"><span data-stu-id="b79c2-321">The sequence number of the current question.</span></span> |
    | <span data-ttu-id="b79c2-322">Root\\Questionnaire\\Question\\Text</span><span class="sxs-lookup"><span data-stu-id="b79c2-322">Root\\Questionnaire\\Question\\Text</span></span>                           | <span data-ttu-id="b79c2-323">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="b79c2-323">String</span></span>      | <span data-ttu-id="b79c2-324">De tekst van de huidige vraag.</span><span class="sxs-lookup"><span data-stu-id="b79c2-324">The text of the current question.</span></span> |
    | <span data-ttu-id="b79c2-325">Root\\Questionnaire\\Question\\Answer</span><span class="sxs-lookup"><span data-stu-id="b79c2-325">Root\\Questionnaire\\Question\\Answer</span></span>                         | <span data-ttu-id="b79c2-326">Recordlijst</span><span class="sxs-lookup"><span data-stu-id="b79c2-326">Record list</span></span> | <span data-ttu-id="b79c2-327">De lijst met antwoorden voor de huidige vraag.</span><span class="sxs-lookup"><span data-stu-id="b79c2-327">The list of answers for the current question.</span></span> |
    | <span data-ttu-id="b79c2-328">Root\\Questionnaire\\Question\\Answer\\CorrectAnswer</span><span class="sxs-lookup"><span data-stu-id="b79c2-328">Root\\Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>          | <span data-ttu-id="b79c2-329">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="b79c2-329">String</span></span>      | <span data-ttu-id="b79c2-330">Een markering die aangeeft of het huidige antwoord correct is.</span><span class="sxs-lookup"><span data-stu-id="b79c2-330">A flag that indicates whether the current answer is correct.</span></span> |
    | <span data-ttu-id="b79c2-331">Root\\Questionnaire\\Question\\Answer\\Points</span><span class="sxs-lookup"><span data-stu-id="b79c2-331">Root\\Questionnaire\\Question\\Answer\\Points</span></span>                 | <span data-ttu-id="b79c2-332">Real-modus</span><span class="sxs-lookup"><span data-stu-id="b79c2-332">Real</span></span>        | <span data-ttu-id="b79c2-333">De punten die worden verdiend wanneer het huidige antwoord wordt geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="b79c2-333">The points that are earned when the current answer is selected.</span></span> |
    | <span data-ttu-id="b79c2-334">Root\\Questionnaire\\Question\\Answer\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="b79c2-334">Root\\Questionnaire\\Question\\Answer\\SequenceNumber</span></span>         | <span data-ttu-id="b79c2-335">Geheel getal</span><span class="sxs-lookup"><span data-stu-id="b79c2-335">Integer</span></span>     | <span data-ttu-id="b79c2-336">Het volgnummer van het huidige antwoord.</span><span class="sxs-lookup"><span data-stu-id="b79c2-336">The sequence number of the current answer.</span></span> |
    | <span data-ttu-id="b79c2-337">Root\\Questionnaire\\Question\\Answer\\Text</span><span class="sxs-lookup"><span data-stu-id="b79c2-337">Root\\Questionnaire\\Question\\Answer\\Text</span></span>                   | <span data-ttu-id="b79c2-338">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="b79c2-338">String</span></span>      | <span data-ttu-id="b79c2-339">De tekst van het huidige antwoord.</span><span class="sxs-lookup"><span data-stu-id="b79c2-339">The text of the current answer.</span></span> |

    <span data-ttu-id="b79c2-340">In de volgende afbeelding ziet u het voltooide bewerkbare gegevensmodel op de pagina **Gegevensmodel ontwerpen**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-340">The following illustration shows the completed editable data model on the **Data model designer** page.</span></span>

    ![Het geconfigureerde gegevensmodel in de ER-gegevensmodelontwerper](./media/er-quick-start1-model2.png)

7. <span data-ttu-id="b79c2-342">Sla de wijzigingen op.</span><span class="sxs-lookup"><span data-stu-id="b79c2-342">Save your changes.</span></span>
8. <span data-ttu-id="b79c2-343">Sluit de pagina **Gegevensmodel ontwerpen**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-343">Close the **Data model designer** page.</span></span>

#### <a name="complete-the-design-of-the-data-model"></a><a name="CompleteDataModel"></a><span data-ttu-id="b79c2-344">Het ontwerp van het gegevensmodel voltooien</span><span class="sxs-lookup"><span data-stu-id="b79c2-344">Complete the design of the data model</span></span>

1. <span data-ttu-id="b79c2-345">Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-345">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="b79c2-346">Selecteer op de pagina **Configuraties** in de structuur met configuraties **Vragenlijstmodel**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-346">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="b79c2-347">Selecteer op het sneltabblad **Versies** de configuratieversie met de status **Concept**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-347">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="b79c2-348">Selecteer **Status wijzigen** \> **Voltooien**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-348">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="b79c2-349">De status van versie 1 van deze configuratie wordt gewijzigd van **Concept** in **Voltooid**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-349">The status of version 1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="b79c2-350">Versie 1 kan niet meer worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="b79c2-350">Version 1 can no longer be changed.</span></span> <span data-ttu-id="b79c2-351">Deze versie bevat het geconfigureerde gegevensmodel en kan worden gebruikt als basis voor andere ER-configuraties.</span><span class="sxs-lookup"><span data-stu-id="b79c2-351">This version contains the configured data model and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="b79c2-352">Versie 2 van deze configuratie wordt gemaakt met de status **Concept**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-352">Version 2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="b79c2-353">U kunt deze versie bewerken om het gegevensmodel **Vragenlijst** aan te passen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-353">You can edit this version to adjust the **Questionnaire** data model.</span></span>

![Versies van de bewerkbare ER-configuratie op de pagina Configuraties](./media/er-quick-start1-model-configuration.png)

<span data-ttu-id="b79c2-355">Zie [Overzicht van Elektronische rapporten (ER)](general-electronic-reporting.md#component-versioning) voor meer informatie over versiebeheer voor ER-configuraties.</span><span class="sxs-lookup"><span data-stu-id="b79c2-355">For more information about versioning for ER configurations, see [Electronic reporting (ER) overview](general-electronic-reporting.md#component-versioning).</span></span>

> [!NOTE]
> <span data-ttu-id="b79c2-356">Het geconfigureerde gegevensmodel is uw verkorte weergave van het bedrijfsdomein **Vragenlijst** en bevat geen relaties naar artefacten die specifiek zijn voor Microsoft Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="b79c2-356">The configured data model is your abstract representation of the **Questionnaire** business domain and contains no relations to artefacts that are specific to Microsoft Dynamics 365 Finance.</span></span>

## <a name="design-a-model-mapping-for-the-configured-data-model"></a><a name="DesignMapping"></a><span data-ttu-id="b79c2-357">Een modeltoewijzing voor het geconfigureerde gegevensmodel ontwerpen</span><span class="sxs-lookup"><span data-stu-id="b79c2-357">Design a model mapping for the configured data model</span></span>

<span data-ttu-id="b79c2-358">Als gebruiker in de rol van ER-ontwikkelaar moet u een nieuwe ER-configuratie maken die een [modeltoewijzings](general-electronic-reporting.md#data-model-and-model-mapping-components)onderdeel bevat voor het gegevensmodel **Vragenlijst**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-358">As a user in the Electronic Reporting Developer role, you must create a new ER configuration that contains a [model mapping](general-electronic-reporting.md#data-model-and-model-mapping-components) component for the **Questionnaire** data model.</span></span> <span data-ttu-id="b79c2-359">Omdat dit onderdeel het geconfigureerde gegevensmodel implementeert voor Finance, is het Finance-specifiek.</span><span class="sxs-lookup"><span data-stu-id="b79c2-359">Because this component implements the configured data model for Finance, it's Finance-specific.</span></span> <span data-ttu-id="b79c2-360">U moet het modeltoewijzingsonderdeel configureren om de toepassingsobjecten op te geven die moeten worden gebruikt voor het invullen met toepassingsgegevens van het geconfigureerde gegevensmodel tijdens runtime.</span><span class="sxs-lookup"><span data-stu-id="b79c2-360">You must configure the model mapping component to specify the application objects that must be used to fill in the configured data model with application data at runtime.</span></span> <span data-ttu-id="b79c2-361">Als u deze taak wilt voltooien, moet u zich bewust zijn van de implementatiedetails van de gegevensstructuur van het bedrijfsdomein van de **Vragenlijst** in Finance.</span><span class="sxs-lookup"><span data-stu-id="b79c2-361">To complete this task, you must be aware of the implementation details of the data structure of the **Questionnaire** business domain in Finance.</span></span>

<span data-ttu-id="b79c2-362">Door de stappen in de sectie [Een nieuwe modeltoewijzingsconfiguratie importeren](#ImportModelMapping) te voltooien, kunt u de vereiste modeltoewijzingsconfiguratie importeren uit het opgegeven XML-bestand.</span><span class="sxs-lookup"><span data-stu-id="b79c2-362">By completing the steps in the [Import a new model mapping configuration](#ImportModelMapping) section that follows, you can import the required model mapping configuration from the provided XML file.</span></span> <span data-ttu-id="b79c2-363">U kunt de stappen in de sectie [Een nieuwe modeltoewijzingsconfiguratie maken](#CreateModelMapping) ook uitvoeren als u een helemaal nieuwe modeltoewijzing wilt ontwerpen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-363">Alternatively, you can complete the steps in the [Create a new model mapping configuration](#CreateModelMapping) section to design this model mapping from scratch.</span></span>

### <a name="import-a-new-model-mapping-configuration"></a><a name="ImportModelMapping"></a><span data-ttu-id="b79c2-364">Een nieuwe configuratie voor de modeltoewijzing importeren</span><span class="sxs-lookup"><span data-stu-id="b79c2-364">Import a new model mapping configuration</span></span>

1. <span data-ttu-id="b79c2-365">Download het bestand [Questionnaires mapping.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) en sla het op uw lokale computer op.</span><span class="sxs-lookup"><span data-stu-id="b79c2-365">Download the [Questionnaires mapping.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="b79c2-366">Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-366">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="b79c2-367">Selecteer in het werkgebied **Elektronische rapportage** de optie **Rapportconfiguraties**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-367">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="b79c2-368">In het actievenster selecteert u **Uitwisselen** \> **Laden uit XML-bestand**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-368">On the Action Pane, select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="b79c2-369">Selecteer **Bladeren** en zoek en selecteer het bestand **Questionnaires mapping.version.1.1.xml**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-369">Select **Browse**, and then find and select the **Questionnaires mapping.version.1.1.xml** file.</span></span>
6. <span data-ttu-id="b79c2-370">Selecteer **OK** om de configuratie te importeren.</span><span class="sxs-lookup"><span data-stu-id="b79c2-370">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="b79c2-371">Als u wilt doorgaan, gaat u naar de volgende procedure [Een nieuwe configuratie voor de modeltoewijzing maken](#CreateModelMapping).</span><span class="sxs-lookup"><span data-stu-id="b79c2-371">To continue, skip the next procedure, [Create a new model mapping configuration](#CreateModelMapping).</span></span>

### <a name="create-a-new-model-mapping-configuration"></a><a name="CreateModelMapping"></a><span data-ttu-id="b79c2-372">Een nieuwe configuratie voor de modeltoewijzing maken</span><span class="sxs-lookup"><span data-stu-id="b79c2-372">Create a new model mapping configuration</span></span>

1. <span data-ttu-id="b79c2-373">Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-373">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="b79c2-374">Selecteer op de pagina **Configuraties** in de structuur met configuraties **Vragenlijstmodel**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-374">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="b79c2-375">Selecteer **Configuratie maken**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-375">Select **Create configuration**.</span></span>
4. <span data-ttu-id="b79c2-376">Voer de volgende stappen uit in het dialoogvenster:</span><span class="sxs-lookup"><span data-stu-id="b79c2-376">In the drop-down dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="b79c2-377">Typ in het veld **Nieuw** **Modeltoewijzing gebaseerd op het gegevensmodel Questionnaires**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-377">In the **New** field, select **Model Mapping based on data model Questionnaires**.</span></span>
    2. <span data-ttu-id="b79c2-378">Voer in het veld **Naam** in **Questionnaires mapping**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-378">In the **Name** field, enter **Questionnaire mapping**.</span></span>
    3. <span data-ttu-id="b79c2-379">Selecteer in het veld **Definitie gegevensmodel** de definitie **Root**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-379">In the **Data model definition** field, select the **Root** definition.</span></span>
    4. <span data-ttu-id="b79c2-380">Selecteer **Configuratie maken** om de configuratie te maken.</span><span class="sxs-lookup"><span data-stu-id="b79c2-380">Select **Create configuration** to create the configuration.</span></span>

#### <a name="design-a-new-model-mapping-component"></a><a name="DesignMappingComponent"></a><span data-ttu-id="b79c2-381">Een nieuw modeltoewijzingsonderdeel ontwerpen</span><span class="sxs-lookup"><span data-stu-id="b79c2-381">Design a new model mapping component</span></span>

1. <span data-ttu-id="b79c2-382">Selecteer op de pagina **Configuraties** in de structuur met configuraties **Vragenlijsttoewijzing**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-382">On the **Configurations** page, in the configuration tree, select **Questionnaire mapping**.</span></span>
2. <span data-ttu-id="b79c2-383">Selecteer **Ontwerper** om de lijst met toewijzingen te openen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-383">Select **Designer** to open the list of mappings.</span></span>
3. <span data-ttu-id="b79c2-384">Selecteer de toewijzing **Questionnaires mapping** die automatisch is toegevoegd voor de definitie **Root**</span><span class="sxs-lookup"><span data-stu-id="b79c2-384">Select the **Questionnaires mapping** mapping that was automatically added for the **Root** definition</span></span>
4. <span data-ttu-id="b79c2-385">Selecteer **Ontwerper** om te beginnen met het configureren van de geselecteerde toewijzing.</span><span class="sxs-lookup"><span data-stu-id="b79c2-385">Select **Designer** to start to configure the selected mapping.</span></span>

<span data-ttu-id="b79c2-386">Er wordt automatisch een nieuwe toewijzing toegevoegd voor de definitie **Root**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-386">A new mapping is automatically added for the **Root** definition.</span></span> <span data-ttu-id="b79c2-387">Deze toewijzing heeft de richting **Naar model**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-387">This mapping has the **To model** direction.</span></span> <span data-ttu-id="b79c2-388">Deze toewijzing kan dus worden gebruikt voor het invullen van een gegevensmodel met vereiste gegevens.</span><span class="sxs-lookup"><span data-stu-id="b79c2-388">Therefore, this mapping can be used to fill in a data model with required data.</span></span>

#### <a name="add-data-sources-to-access-application-tables"></a><a name="AddMmDataSource1"></a><span data-ttu-id="b79c2-389">Gegevensbronnen toevoegen voor toegang tot toepassingstabellen</span><span class="sxs-lookup"><span data-stu-id="b79c2-389">Add data sources to access application tables</span></span>

<span data-ttu-id="b79c2-390">U moet gegevensbronnen configureren om toegang te krijgen tot de toepassingstabellen die vragenlijstdetails bevatten.</span><span class="sxs-lookup"><span data-stu-id="b79c2-390">You must configure data sources to access the application tables that contain questionnaire details.</span></span>

1. <span data-ttu-id="b79c2-391">Selecteer op de pagina **Ontwerper modeltoewijzing** in het deelvenster **Typen gegevensbronnen** **Dynamics 365 for Operations\\Tabelrecords**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-391">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
2. <span data-ttu-id="b79c2-392">Voeg een nieuwe gegevensbron toe die wordt gebruikt om toegang te krijgen tot de tabel KMCollection, waarbij elke record één vragenlijst vertegenwoordigt:</span><span class="sxs-lookup"><span data-stu-id="b79c2-392">Add a new data source that will be used to access the KMCollection table, where every record represents a single questionnaire:</span></span>

    1. <span data-ttu-id="b79c2-393">Selecteer **Basis toevoegen** in het deelvenster **Gegevensbronnen**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-393">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="b79c2-394">Voer in het dialoogvenster in het veld **Naam** de tekst **Vragenlijst** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-394">In dialog box, in the **Name** field, enter **Questionnaire**.</span></span>
    3. <span data-ttu-id="b79c2-395">Voer in het veld **Tabel** **KMCollection** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-395">In the **Table** field, enter **KMCollection**.</span></span>
    4. <span data-ttu-id="b79c2-396">Stel de optie **Vragen om query** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-396">Set the **Ask for query** option to **Yes**.</span></span> <span data-ttu-id="b79c2-397">Tijdens runtime kunt u vervolgens [filter](../../fin-ops/get-started/advanced-filtering-query-options.md)opties voor deze tabel opgeven in het dialoogvenster voor de systeemquery.</span><span class="sxs-lookup"><span data-stu-id="b79c2-397">You will then be able to specify [filtering](../../fin-ops/get-started/advanced-filtering-query-options.md) options for this table in the system query dialog box at runtime.</span></span>
    5. <span data-ttu-id="b79c2-398">Klik op **OK** om de nieuwe gegevensbron toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-398">Select **OK** to add the new data source.</span></span>

3. <span data-ttu-id="b79c2-399">Selecteer in het deelvenster **Typen gegevensbronnen** **Dynamics 365 for Operations\\Tabelrecords**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-399">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
4. <span data-ttu-id="b79c2-400">Voeg een nieuwe gegevensbron toe die wordt gebruikt om toegang te krijgen tot de tabel KMQuestion, waarbij elke record één vraag in een vragenlijst vertegenwoordigt:</span><span class="sxs-lookup"><span data-stu-id="b79c2-400">Add a new data source that will be used to access the KMQuestion table, where every record represents a single question in a questionnaire:</span></span>

    1. <span data-ttu-id="b79c2-401">Selecteer **Basis toevoegen** in het deelvenster **Gegevensbronnen**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-401">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="b79c2-402">Voer in het dialoogvenster in het veld **Naam** de tekst **Vraag** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-402">In the dialog box, in the **Name** field, enter **Question**.</span></span>
    3. <span data-ttu-id="b79c2-403">Voer in het veld **Tabel** **KMQuestion** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-403">In the **Table** field, enter **KMQuestion**.</span></span>
    4. <span data-ttu-id="b79c2-404">Klik op **OK** om de nieuwe gegevensbron toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-404">Select **OK** to add the new data source.</span></span>

5. <span data-ttu-id="b79c2-405">Selecteer in het deelvenster **Typen gegevensbronnen** **Dynamics 365 for Operations\\Tabelrecords**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-405">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
6. <span data-ttu-id="b79c2-406">Voeg een nieuwe gegevensbron toe die wordt gebruikt om toegang te krijgen tot de tabel KMAnswer, waarbij elke record één antwoord op een vraag in een vragenlijst vertegenwoordigt:</span><span class="sxs-lookup"><span data-stu-id="b79c2-406">Add a new data source try that will be used to access the KMAnswer table, where every record represents a single answer to a question in a questionnaire:</span></span>

    1. <span data-ttu-id="b79c2-407">Selecteer **Basis toevoegen** in het deelvenster **Gegevensbronnen**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-407">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="b79c2-408">Voer in het veld **Naam** de tekst **Antwoord** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-408">In the **Name** field, enter **Answer**.</span></span>
    3. <span data-ttu-id="b79c2-409">Voer in het veld **Tabel** **KMAnswer** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-409">In the **Table** field, enter **KMAnswer**.</span></span>
    4. <span data-ttu-id="b79c2-410">Klik op **OK** om de nieuwe gegevensbron toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-410">Select **OK** to add the new data source.</span></span>

7. <span data-ttu-id="b79c2-411">Selecteer in het deelvenster **Typen gegevensbronnen** **Functies\\Berekend veld**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-411">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
8. <span data-ttu-id="b79c2-412">Voeg een nieuw berekend veld toe dat wordt gebruikt om toegang te krijgen tot een record in de tabel KMQuestionResultGroup vanuit elke record van de bovenliggende KMCollection-tabel:</span><span class="sxs-lookup"><span data-stu-id="b79c2-412">Add a new calculated field that will be used to access a record of the KMQuestionResultGroup table from every record of the parent KMCollection table:</span></span>

    1. <span data-ttu-id="b79c2-413">Selecteer **Vragenlijst** in het deelvenster **Gegevensbronnen**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-413">In the **Data sources** pane, select **Questionnaire**.</span></span>
    2. <span data-ttu-id="b79c2-414">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-414">Select **Add**.</span></span>
    3. <span data-ttu-id="b79c2-415">Voer in het dialoogvenster in het veld **Naam** **\$ResultGroup** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-415">In the dialog box, in the **Name** field, enter **\$ResultGroup**.</span></span>
    4. <span data-ttu-id="b79c2-416">Selecteer **Formule bewerken**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-416">Select **Edit formula**.</span></span>
    5. <span data-ttu-id="b79c2-417">Voer in de [ER-formule-editor](general-electronic-reporting-formula-designer.md), in het veld **Formule**, **FIRSTORNULL(\@.'\<Relations'.KMQuestionResultGroup)** in om het [pad](er-formula-language.md#paths) van de één-op-veel-relatie te gebruiken tussen de tabellen KMCollection en KMQuestionResultGroup.</span><span class="sxs-lookup"><span data-stu-id="b79c2-417">In the [ER formula editor](general-electronic-reporting-formula-designer.md), in the **Formula** field, enter **FIRSTORNULL(\@.'\<Relations'.KMQuestionResultGroup)** to use the [path](er-formula-language.md#paths) of the one-to-many relation between the KMCollection and KMQuestionResultGroup tables.</span></span>
    6. <span data-ttu-id="b79c2-418">Selecteer **Opslaan** en sluit de formule-editor.</span><span class="sxs-lookup"><span data-stu-id="b79c2-418">Select **Save**, and close the formula editor.</span></span>
    7. <span data-ttu-id="b79c2-419">Klik op **OK** om het nieuwe berekende veld toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-419">Select **OK** to add the new calculated field.</span></span>

9. <span data-ttu-id="b79c2-420">Selecteer in het deelvenster **Typen gegevensbronnen** **Functies\\Berekend veld**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-420">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
10. <span data-ttu-id="b79c2-421">Voeg een nieuw berekend veld toe dat wordt gebruikt om toegang te krijgen tot vraagrecords in de tabel KMQuestion vanuit elke record van de bovenliggende tabel KMCollectionQuestion:</span><span class="sxs-lookup"><span data-stu-id="b79c2-421">Add a new calculated field that will be used to access question records of the KMQuestion table from every record of the parent KMCollectionQuestion table:</span></span>

    1. <span data-ttu-id="b79c2-422">Selecteer **Vragenlijst** in het deelvenster **Gegevensbronnen**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-422">In the **Data sources** pane, select **Questionnaire**.</span></span>
    2. <span data-ttu-id="b79c2-423">Vouw het knooppunt **\<Relaties** uit dat één-op-veel-relaties bevat van de tabel KMCollection.</span><span class="sxs-lookup"><span data-stu-id="b79c2-423">Expand the **\<Relations** node that contains one-to-many relations of the KMCollection table.</span></span>
    3. <span data-ttu-id="b79c2-424">Selecteer de gerelateerde tabel **KMCollectionQuestion** en selecteer vervolgens **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-424">Select the related **KMCollectionQuestion** table, and then select **Add**.</span></span>
    4. <span data-ttu-id="b79c2-425">Voer in het dialoogvenster in het veld **Naam** **\$Question** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-425">In the dialog box, in the **Name** field, enter **\$Question**.</span></span>
    5. <span data-ttu-id="b79c2-426">Selecteer **Formule bewerken**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-426">Select **Edit formula**.</span></span>
    6. <span data-ttu-id="b79c2-427">Voer in de formule-editor, in het veld **Formule** **FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))** in om de desbetreffende vraagrecords uit de tabel KMQuestion te retourneren..</span><span class="sxs-lookup"><span data-stu-id="b79c2-427">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (FILTER(Question, Question.kmQuestionId = \@.kmQuestionId))** to return the appropriate question records from the KMQuestion table.</span></span>
    7. <span data-ttu-id="b79c2-428">Selecteer **Opslaan** en sluit de formule-editor.</span><span class="sxs-lookup"><span data-stu-id="b79c2-428">Select **Save**, and close the formula editor.</span></span>
    8. <span data-ttu-id="b79c2-429">Klik op **OK** om het nieuwe berekende veld toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-429">Select **OK** to add the new calculated field.</span></span>

11. <span data-ttu-id="b79c2-430">Selecteer in het deelvenster **Typen gegevensbronnen** **Functies\\Berekend veld**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-430">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
12. <span data-ttu-id="b79c2-431">Voeg een nieuw berekend veld toe dat wordt gebruikt om toegang te krijgen tot antwoordrecords in de tabel KMAnswer vanuit elke record van de bovenliggende tabel KMQuestion:</span><span class="sxs-lookup"><span data-stu-id="b79c2-431">Add a new calculated field that will be used to access answer records of the KMAnswer table from every record of the parent KMQuestion table:</span></span>

    1. <span data-ttu-id="b79c2-432">Selecteer in het deelvenster **Gegevensbronnen** **Questionnaire.\<Relations.KMCollectionQuestion.\$Question**, en vervolgens **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-432">In the **Data sources** pane, select **Questionnaire.\<Relations.KMCollectionQuestion.\$Question**, and then select **Add**.</span></span>
    2. <span data-ttu-id="b79c2-433">Voer in het dialoogvenster in het veld **Naam** **\$Answer** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-433">In the dialog box, in the **Name** field, enter **\$Answer**.</span></span>
    3. <span data-ttu-id="b79c2-434">Selecteer **Formule bewerken**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-434">Select **Edit formula**.</span></span>
    4. <span data-ttu-id="b79c2-435">Voer in de formule-editor, in het veld **Formule** **FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)** in om de desbetreffende antwoordrecords uit de tabel KMAnswer te retourneren..</span><span class="sxs-lookup"><span data-stu-id="b79c2-435">In the formula editor, in the **Formula** field, enter **FILTER (Answer, Answer.kmAnswerCollectionId = \@.kmAnswerCollectionId)** to return the appropriate answer records from the KMAnswer table.</span></span>
    5. <span data-ttu-id="b79c2-436">Selecteer **Opslaan** en sluit de formule-editor.</span><span class="sxs-lookup"><span data-stu-id="b79c2-436">Select **Save**, and close the formula editor.</span></span>
    6. <span data-ttu-id="b79c2-437">Klik op **OK** om het nieuwe berekende veld toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-437">Select **OK** to add the new calculated field.</span></span>

13. <span data-ttu-id="b79c2-438">Selecteer in het deelvenster **Typen gegevensbronnen** **Dynamics 365 for Operations\\Tabel**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-438">In the **Data source types** pane, select **Dynamics 365 for Operations\\Table**.</span></span>
14. <span data-ttu-id="b79c2-439">Voeg een nieuwe gegevensbron toe die wordt gebruikt om toegang te krijgen tot methoden in de tabel CompanyInfo.</span><span class="sxs-lookup"><span data-stu-id="b79c2-439">Add a new data source that will be used to access methods of the CompanyInfo table.</span></span> <span data-ttu-id="b79c2-440">De methode **find()** in deze tabel retourneert een record die een bedrijf vertegenwoordigt van het huidige Finance-exemplaar waarvoor deze toewijzing wordt aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-440">Note that the **find()** method of this table returns a record that represents a company of the current Finance instance that this mapping is called in the context of.</span></span>

    1. <span data-ttu-id="b79c2-441">Selecteer **Basis toevoegen** in het deelvenster **Gegevensbronnen**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-441">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="b79c2-442">Voer in het dialoogvenster in het veld **Naam** **CompanyInfo** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-442">In the dialog box, in the **Name** field, enter **CompanyInfo**.</span></span>
    3. <span data-ttu-id="b79c2-443">Voer in het veld **Tabel** **CompanyInfo** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-443">In the **Table** field, enter **CompanyInfo**.</span></span>
    4. <span data-ttu-id="b79c2-444">Klik op **OK** om de nieuwe gegevensbron toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-444">Select **OK** to add the new data source.</span></span>

#### <a name="add-data-sources-to-access-application-enumerations"></a><a name="AddMmDataSource2"></a><span data-ttu-id="b79c2-445">Gegevensbronnen toevoegen voor toegang tot toepassingsopsommingen</span><span class="sxs-lookup"><span data-stu-id="b79c2-445">Add data sources to access application enumerations</span></span>

<span data-ttu-id="b79c2-446">U moet gegevensbronnen configureren om toegang te krijgen tot toepassingsopsommingen en hun waarden te vergelijken met waarden van velden van het type **Opsomming** in de toepassingstabellen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-446">You must configure data sources to access application enumerations and compare their values with values of fields of the **Enumeration** type in the application tables.</span></span> <span data-ttu-id="b79c2-447">U moet het resultaat van de vergelijking gebruiken om de relevante velden van het gegevensmodel in te vullen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-447">You must use the result of the comparison to fill in appropriate fields of the data model.</span></span>

1. <span data-ttu-id="b79c2-448">Selecteer op de pagina **Ontwerper modeltoewijzing** in het deelvenster **Typen gegevensbronnen** **Dynamics 365 for Operations\\Opsomming**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-448">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Enumeration**.</span></span>
2. <span data-ttu-id="b79c2-449">Voeg een nieuwe gegevensbron toe die wordt gebruikt om toegang te krijgen tot waarden van de opsomming **EnumAppNoYes**:</span><span class="sxs-lookup"><span data-stu-id="b79c2-449">Add a new data source that will be used to access values of the **EnumAppNoYes** enumeration:</span></span>

    1. <span data-ttu-id="b79c2-450">Selecteer **Basis toevoegen** in het deelvenster **Gegevensbronnen**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-450">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="b79c2-451">Voer in het dialoogvenster in het veld **Naam** **EnumAppNoYes** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-451">In the dialog box, in the **Name** field, enter **EnumAppNoYes**.</span></span>
    3. <span data-ttu-id="b79c2-452">Voer in het veld **Opsomming** **NoYes** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-452">In the **Enumeration** field, enter **NoYes**.</span></span>
    4. <span data-ttu-id="b79c2-453">Klik op **OK** om de nieuwe gegevensbron toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-453">Select **OK** to add the new data source.</span></span>

3. <span data-ttu-id="b79c2-454">Selecteer in het deelvenster **Typen gegevensbronnen** **Dynamics 365 for Operations\\Opsomming**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-454">In the **Data source types** pane, select **Dynamics 365 for Operations\\Enumeration**.</span></span>
4. <span data-ttu-id="b79c2-455">Voeg een nieuwe gegevensbron toe die wordt gebruikt om toegang te krijgen tot de waarden van de opsomming **KMCollectionQuestionMode**:</span><span class="sxs-lookup"><span data-stu-id="b79c2-455">Add a new data source that will be used to access the values of the **KMCollectionQuestionMode** enumeration:</span></span>

    1. <span data-ttu-id="b79c2-456">Selecteer **Basis toevoegen** in het deelvenster **Gegevensbronnen**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-456">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="b79c2-457">Voer in het dialoogvenster in het veld **Naam** **EnumAppQuestionOrder** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-457">In the dialog box, in the **Name** field, enter **EnumAppQuestionOrder**.</span></span>
    3. <span data-ttu-id="b79c2-458">Voer in het veld **Opsomming** **KMCollectionQuestionMode** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-458">In the **Enumeration** field, enter **KMCollectionQuestionMode**.</span></span>
    4. <span data-ttu-id="b79c2-459">Klik op **OK** om de nieuwe gegevensbron toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-459">Select **OK** to add the new data source.</span></span>

#### <a name="add-er-labels-to-generate-a-report-in-a-specified-language"></a><a name="AddMmLabels"></a><span data-ttu-id="b79c2-460">ER-labels toevoegen om een rapport in een opgegeven taal te genereren</span><span class="sxs-lookup"><span data-stu-id="b79c2-460">Add ER labels to generate a report in a specified language</span></span>

<span data-ttu-id="b79c2-461">U kunt ER-labels toevoegen om een aantal van uw gegevensbronnen te configureren voor het retourneren van waarden die afhankelijk zijn van de taal die is gedefinieerd in de context van het aanroepen van de modeltoewijzing.</span><span class="sxs-lookup"><span data-stu-id="b79c2-461">You can add ER labels to configure some of your data sources to return values that depend on the language that is defined in the context of the model mapping's call.</span></span>

1. <span data-ttu-id="b79c2-462">Selecteer op de pagina **Ontwerper modeltoewijzing** in het deelvenster **Gegevensbronnen** de optie **Antwoord** en vervolgens **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-462">On the **Model mapping designer** page, in the **Data sources** pane, select **Answer**, and then select **Edit**.</span></span>
2. <span data-ttu-id="b79c2-463">Activeer het veld **Label**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-463">Activate the **Label** field.</span></span>
3. <span data-ttu-id="b79c2-464">Selecteer **Vertalen**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-464">Select **Translate**.</span></span>
4. <span data-ttu-id="b79c2-465">Voer de volgende stappen uit in het dialoogvenster **Tekstvertaling**:</span><span class="sxs-lookup"><span data-stu-id="b79c2-465">In the **Text translation** dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="b79c2-466">Voer in het veld **Label-id** **PositiveAnswer** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-466">In the **Label Id** field, enter **PositiveAnswer**.</span></span>
    2. <span data-ttu-id="b79c2-467">Voer in het veld **Tekst in standaardtaal** **Ja** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-467">In the **Text in default language** field, enter **Yes**.</span></span>
    3. <span data-ttu-id="b79c2-468">Selecteer **Vertalen**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-468">Select **Translate**.</span></span>
    4. <span data-ttu-id="b79c2-469">Voer in het veld **Label-id** **NegativeAnswer** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-469">In the **Label Id** field, enter **NegativeAnswer**.</span></span>
    5. <span data-ttu-id="b79c2-470">Voer in het veld **Tekst in standaardtaal** **Nee** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-470">In the **Text in default language** field, enter **No**.</span></span>
    6. <span data-ttu-id="b79c2-471">Selecteer **Vertalen**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-471">Select **Translate**.</span></span>

5. <span data-ttu-id="b79c2-472">Sluit het dialoogvenster **Tekstvertaling**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-472">Close the **Text translation** dialog box.</span></span>
6. <span data-ttu-id="b79c2-473">Selecteer **Annuleren**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-473">Select **Cancel**.</span></span>

![ER-labels toevoegen voor de bewerkbare modeltoewijzing](./media/er-quick-start1-adding-labels.png)

<span data-ttu-id="b79c2-475">U hebt voor de standaardtaal alleen ER-labels ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="b79c2-475">You've entered ER labels only for the default language.</span></span> <span data-ttu-id="b79c2-476">Zie [Meertalige rapporten ontwerpen](er-design-multilingual-reports.md) voor informatie over hoe ER-labels kunnen worden vertaald in andere talen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-476">For information about how ER labels can be translated into other languages, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

#### <a name="add-a-data-source-to-transform-the-results-of-comparing-enumeration-values-to-a-text-value"></a><a name="AddMmDataSource3"></a><span data-ttu-id="b79c2-477">Een gegevensbron toevoegen om de resultaten van het vergelijken van opsommingswaarden met een tekstwaarde te transformeren</span><span class="sxs-lookup"><span data-stu-id="b79c2-477">Add a data source to transform the results of comparing enumeration values to a text value</span></span>

<span data-ttu-id="b79c2-478">Omdat u de resultaten van de vergelijking tussen opsommingswaarden en tekstwaarden diverse keren moet omrekenen voor verschillen bronnen, is het een goed idee om deze logica als één gegevensbron te configureren.</span><span class="sxs-lookup"><span data-stu-id="b79c2-478">Because you must transform the results of the comparison between enumeration values and text values several times for difference sources, it's a good idea to configure this logic as a single data source.</span></span> <span data-ttu-id="b79c2-479">Als u deze gegevens bron herbruikbaar wilt maken, moet u deze vervolgens wel configureren als de gegevensbron met parameters.</span><span class="sxs-lookup"><span data-stu-id="b79c2-479">However, to make this data source reusable, you must then configure it as the parametrized data source.</span></span> <span data-ttu-id="b79c2-480">Zie [Ondersteuning bieden voor parameteraanroepen van ER-gegevensbronnen van het Berekende veld-type](er-calculated-field-type.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="b79c2-480">For more information, see [Support parameterized calls of ER data sources of the Calculated field type](er-calculated-field-type.md).</span></span>

1. <span data-ttu-id="b79c2-481">Selecteer op de pagina **Ontwerper modeltoewijzing** in het deelvenster **Typen gegevensbronnen** **Algemeen\\Lege container**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-481">On the **Model mapping designer** page, in the **Data source types** pane, select **General\\Empty container**.</span></span>
2. <span data-ttu-id="b79c2-482">Een nieuwe gegevensbron voor een container toevoegen:</span><span class="sxs-lookup"><span data-stu-id="b79c2-482">Add a new container data source:</span></span>

    1. <span data-ttu-id="b79c2-483">Selecteer **Basis toevoegen** in het deelvenster **Gegevensbronnen**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-483">In the **Data sources** pane, select **Add root**.</span></span>
    2. <span data-ttu-id="b79c2-484">Voer in het dialoogvenster in het veld **Naam** de tekst **Helper** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-484">In the dialog box, in the **Name** field, enter **Helper**.</span></span>
    3. <span data-ttu-id="b79c2-485">Klik op **OK** om de nieuwe gegevensbron voor de container toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-485">Select **OK** to add the new container data source.</span></span>

3. <span data-ttu-id="b79c2-486">Selecteer in het deelvenster **Typen gegevensbronnen** **Functies\\Berekend veld**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-486">In the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
4. <span data-ttu-id="b79c2-487">Een nieuwe gegevensbron toevoegen:</span><span class="sxs-lookup"><span data-stu-id="b79c2-487">Add a new data source:</span></span>

    1. <span data-ttu-id="b79c2-488">Selecteer **Helper** in het deelvenster **Gegevensbron**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-488">In the **Data sources** pane, select **Helper**.</span></span>
    2. <span data-ttu-id="b79c2-489">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-489">Select **Add**.</span></span>
    3. <span data-ttu-id="b79c2-490">Voer in het dialoogvenster in het veld **Naam** **NoYesEnumToString** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-490">In the dialog box, in the **Name** field, enter **NoYesEnumToString**.</span></span>
    4. <span data-ttu-id="b79c2-491">Selecteer **Formule bewerken**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-491">Select **Edit formula**.</span></span>
    5. <span data-ttu-id="b79c2-492">Selecteer in de formule-editor **Parameters**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-492">In the formula editor, select **Parameters**.</span></span>
    6. <span data-ttu-id="b79c2-493">Voer de volgende stappen uit om parameters op te geven voor de geconfigureerde expressie:</span><span class="sxs-lookup"><span data-stu-id="b79c2-493">Follow these steps to specify parameters for the configured expression:</span></span>

        1. <span data-ttu-id="b79c2-494">Selecteer **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-494">Select **New**.</span></span>
        2. <span data-ttu-id="b79c2-495">Voer in het dialoogvenster in het veld **Naam** de tekst **Argument** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-495">In the dialog box, in the **Name** field, enter **Argument**.</span></span>
        3. <span data-ttu-id="b79c2-496">Selecteer in het veld **Type** het gegevenstype **Booleaans**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-496">In the **Type** field, select the **Boolean** data type.</span></span>
        4. <span data-ttu-id="b79c2-497">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-497">Select **OK**.</span></span>

    7. <span data-ttu-id="b79c2-498">Voer in het veld **Formule** **IF (Argument = true, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")** om de tekst van het desbetreffende ER-label te retourneren, afhankelijk van de taal van de uitvoeringscontext en de waarde van de opgegeven parameter.</span><span class="sxs-lookup"><span data-stu-id="b79c2-498">In the **Formula** field, enter **IF (Argument = true, \@"GER\_LABEL:PositiveAnswer", \@"GER\_LABEL:NegativeAnswer")** to return the text of the appropriate ER label, depending on the language of the execution context and value of the specified parameter.</span></span>
    8. <span data-ttu-id="b79c2-499">Selecteer **Opslaan** en sluit de formule-editor.</span><span class="sxs-lookup"><span data-stu-id="b79c2-499">Select **Save**, and close the formula editor.</span></span>
    9. <span data-ttu-id="b79c2-500">Klik op **OK** om de nieuwe gegevensbron toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-500">Select **OK** to add the new data source.</span></span>

![Geconfigureerde modeltoewijzing in de ER-ontwerper voor de modeltoewijzing](./media/er-quick-start1-added-data-sources.png)

#### <a name="bind-data-sources-to-data-model-fields"></a><a name="AddMmBindings1"></a><span data-ttu-id="b79c2-502">Gegevensbronnen binden aan gegevensmodelvelden</span><span class="sxs-lookup"><span data-stu-id="b79c2-502">Bind data sources to data model fields</span></span>

<span data-ttu-id="b79c2-503">U moet de geconfigureerde gegevensbronnen binden aan de velden van het gegevensmodel om op te geven hoe het gegevensmodel tijdens runtime moet worden gevuld met toepassingsgegevens.</span><span class="sxs-lookup"><span data-stu-id="b79c2-503">You must bind the configured data sources to the fields of the data model to specify how the data model will by filled in with application data at runtime.</span></span>

1. <span data-ttu-id="b79c2-504">Selecteer op de pagina **Ontwerper modeltoewijzing** in het deelvenster **Gegevensmodel** **CompanyName**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-504">On the **Model mapping designer** page, in the **Data model** pane, select **CompanyName**.</span></span>
2. <span data-ttu-id="b79c2-505">Vouw **CompanyInfo** uit in het deelvenster **Gegevensbronnen** en voer vervolgens de volgende stappen uit:</span><span class="sxs-lookup"><span data-stu-id="b79c2-505">In the **Data sources** pane, expand **CompanyInfo**, and then follow these steps:</span></span>

    1. <span data-ttu-id="b79c2-506">Vouw het knooppunt **CompanyInfo.find()** uit dat de methode **find()** van de tabel CompanyInfo vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="b79c2-506">Expand the **CompanyInfo.find()** node that represents the **find()** method of the CompanyInfo table.</span></span>
    2. <span data-ttu-id="b79c2-507">Selecteer **CompanyInfo.find().Name**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-507">Select **CompanyInfo.find().Name**.</span></span>
    3. <span data-ttu-id="b79c2-508">Selecteer **Binden** om de naam van het bedrijf in te vullen waarvoor de geconfigureerde modeltoewijzing tijdens runtime wordt aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-508">Select **Bind** to fill in the name of the company that the configured model mapping is called in the context of at runtime.</span></span>

3. <span data-ttu-id="b79c2-509">Selecteer **Vragenlijst** in het deelvenster **Gegevensmodel**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-509">In the **Data model** pane, select **Questionnaire**.</span></span>
4. <span data-ttu-id="b79c2-510">Selecteer in het deelvenster **Gegevensbronnen** **Vragenlijst** en selecteer **Binden** om de vragenlijstrecords in te vullen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-510">In the **Data sources** pane, select **Questionnaire**, and then select **Bind** to fill in questionnaire records.</span></span>
5. <span data-ttu-id="b79c2-511">Vouw **Vragenlijst** uit in het deelvenster **Gegevensmodel** en voer de volgende stappen uit:</span><span class="sxs-lookup"><span data-stu-id="b79c2-511">In the **Data model** pane, expand **Questionnaire**, and then follow these steps:</span></span>

    1. <span data-ttu-id="b79c2-512">Selecteer **Actief** in het deelvenster **Gegevensmodel**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-512">In the **Data model** pane, select **Active**.</span></span>
    2. <span data-ttu-id="b79c2-513">Selecteer **Bewerken** in het deelvenster **Gegevensmodel**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-513">In the **Data model** pane, select **Edit**.</span></span>
    3. <span data-ttu-id="b79c2-514">Voer in het veld **Formule** **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)** in om de tekstafhankelijke en taalafhankelijke resultaten van de vergelijking tussen opsommingswaarden te vullen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-514">In the **Formula** field, enter **Helper.NoYesEnumToString (\@.Active = EnumAppNoYes.Yes)** to fill the text-dependent and language-dependent result of the comparison between enumeration values.</span></span>

6. <span data-ttu-id="b79c2-515">Blijf de gegevensbronnen op dezelfde manier binden aan gegevensmodelvelden totdat u het volgende resultaat bereikt.</span><span class="sxs-lookup"><span data-stu-id="b79c2-515">Continue to bind data sources to data model fields in the same manner until you achieve the following result.</span></span>

    | <span data-ttu-id="b79c2-516">Veldpad</span><span class="sxs-lookup"><span data-stu-id="b79c2-516">Field path</span></span>                                              | <span data-ttu-id="b79c2-517">Gegevenstype</span><span class="sxs-lookup"><span data-stu-id="b79c2-517">Data type</span></span>   | <span data-ttu-id="b79c2-518">Actie</span><span class="sxs-lookup"><span data-stu-id="b79c2-518">Action</span></span> | <span data-ttu-id="b79c2-519">Bindingsexpressie</span><span class="sxs-lookup"><span data-stu-id="b79c2-519">Binding expression</span></span> |
    |---------------------------------------------------------|-------------|--------|--------------------|
    | <span data-ttu-id="b79c2-520">CompanyName</span><span class="sxs-lookup"><span data-stu-id="b79c2-520">CompanyName</span></span>                                             | <span data-ttu-id="b79c2-521">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="b79c2-521">String</span></span>      | <span data-ttu-id="b79c2-522">Binden</span><span class="sxs-lookup"><span data-stu-id="b79c2-522">Bind</span></span>   | <span data-ttu-id="b79c2-523">CompanyInfo.'find()'.Name</span><span class="sxs-lookup"><span data-stu-id="b79c2-523">CompanyInfo.'find()'.Name</span></span> |
    | <span data-ttu-id="b79c2-524">Vragenlijst</span><span class="sxs-lookup"><span data-stu-id="b79c2-524">Questionnaire</span></span>                                           | <span data-ttu-id="b79c2-525">Recordlijst</span><span class="sxs-lookup"><span data-stu-id="b79c2-525">Record list</span></span> | <span data-ttu-id="b79c2-526">Binden</span><span class="sxs-lookup"><span data-stu-id="b79c2-526">Bind</span></span>   | <span data-ttu-id="b79c2-527">Vragenlijst</span><span class="sxs-lookup"><span data-stu-id="b79c2-527">Questionnaire</span></span> |
    | <span data-ttu-id="b79c2-528">Questionnaire\\Active</span><span class="sxs-lookup"><span data-stu-id="b79c2-528">Questionnaire\\Active</span></span>                                   | <span data-ttu-id="b79c2-529">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="b79c2-529">String</span></span>      | <span data-ttu-id="b79c2-530">Bewerken</span><span class="sxs-lookup"><span data-stu-id="b79c2-530">Edit</span></span>   | <span data-ttu-id="b79c2-531">Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="b79c2-531">Helper.NoYesEnumToString(\@.active = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="b79c2-532">Questionnaire\\Code</span><span class="sxs-lookup"><span data-stu-id="b79c2-532">Questionnaire\\Code</span></span>                                     | <span data-ttu-id="b79c2-533">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="b79c2-533">String</span></span>      | <span data-ttu-id="b79c2-534">Binden</span><span class="sxs-lookup"><span data-stu-id="b79c2-534">Bind</span></span>   | <span data-ttu-id="b79c2-535">\@.kmCollectionId</span><span class="sxs-lookup"><span data-stu-id="b79c2-535">\@.kmCollectionId</span></span> |
    | <span data-ttu-id="b79c2-536">Questionnaire\\Description</span><span class="sxs-lookup"><span data-stu-id="b79c2-536">Questionnaire\\Description</span></span>                              | <span data-ttu-id="b79c2-537">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="b79c2-537">String</span></span>      | <span data-ttu-id="b79c2-538">Binden</span><span class="sxs-lookup"><span data-stu-id="b79c2-538">Bind</span></span>   | <span data-ttu-id="b79c2-539">\@.Description</span><span class="sxs-lookup"><span data-stu-id="b79c2-539">\@.Description</span></span> |
    | <span data-ttu-id="b79c2-540">Questionnaire\\QuestionnaireType</span><span class="sxs-lookup"><span data-stu-id="b79c2-540">Questionnaire\\QuestionnaireType</span></span>                        | <span data-ttu-id="b79c2-541">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="b79c2-541">String</span></span>      | <span data-ttu-id="b79c2-542">Binden</span><span class="sxs-lookup"><span data-stu-id="b79c2-542">Bind</span></span>   | <span data-ttu-id="b79c2-543">\@.'&gt;Relations'.kmCollectionTypeId.Description</span><span class="sxs-lookup"><span data-stu-id="b79c2-543">\@.'&gt;Relations'.kmCollectionTypeId.Description</span></span> |
    | <span data-ttu-id="b79c2-544">Questionnaire\\QuestionOrder</span><span class="sxs-lookup"><span data-stu-id="b79c2-544">Questionnaire\\QuestionOrder</span></span>                            | <span data-ttu-id="b79c2-545">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="b79c2-545">String</span></span>      | <span data-ttu-id="b79c2-546">Bewerken</span><span class="sxs-lookup"><span data-stu-id="b79c2-546">Edit</span></span>   | <span data-ttu-id="b79c2-547">CASE (\@.questionMode,</span><span class="sxs-lookup"><span data-stu-id="b79c2-547">CASE (\@.questionMode,</span></span><br><span data-ttu-id="b79c2-548">EnumAppQuestionOrder.Conditional, "Conditional",</span><span class="sxs-lookup"><span data-stu-id="b79c2-548">EnumAppQuestionOrder.Conditional, "Conditional",</span></span><br><span data-ttu-id="b79c2-549">EnumAppQuestionOrder.Random, "Random (percentage in questionnaire)",</span><span class="sxs-lookup"><span data-stu-id="b79c2-549">EnumAppQuestionOrder.Random, "Random (percentage in questionnaire)",</span></span><br><span data-ttu-id="b79c2-550">EnumAppQuestionOrder.RandomGroup, "Random (percentage in result groups)",</span><span class="sxs-lookup"><span data-stu-id="b79c2-550">EnumAppQuestionOrder.RandomGroup, "Random (percentage in result groups)",</span></span><br><span data-ttu-id="b79c2-551">EnumAppQuestionOrder.Sequence, "Sequential",</span><span class="sxs-lookup"><span data-stu-id="b79c2-551">EnumAppQuestionOrder.Sequence, "Sequential",</span></span><br><span data-ttu-id="b79c2-552">"")</span><span class="sxs-lookup"><span data-stu-id="b79c2-552">"")</span></span> |
    | <span data-ttu-id="b79c2-553">Questionnaire\\ResultsGroup</span><span class="sxs-lookup"><span data-stu-id="b79c2-553">Questionnaire\\ResultsGroup</span></span>                             | <span data-ttu-id="b79c2-554">Registreren</span><span class="sxs-lookup"><span data-stu-id="b79c2-554">Record</span></span>      |        | |
    | <span data-ttu-id="b79c2-555">Questionnaire\\ResultsGroup\\Code</span><span class="sxs-lookup"><span data-stu-id="b79c2-555">Questionnaire\\ResultsGroup\\Code</span></span>                       | <span data-ttu-id="b79c2-556">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="b79c2-556">String</span></span>      | <span data-ttu-id="b79c2-557">Binden</span><span class="sxs-lookup"><span data-stu-id="b79c2-557">Bind</span></span>   | <span data-ttu-id="b79c2-558">\@.'\$ResultGroup'.kmQuestionResultGroupId</span><span class="sxs-lookup"><span data-stu-id="b79c2-558">\@.'\$ResultGroup'.kmQuestionResultGroupId</span></span> |
    | <span data-ttu-id="b79c2-559">Questionnaire\\ResultsGroup\\Description</span><span class="sxs-lookup"><span data-stu-id="b79c2-559">Questionnaire\\ResultsGroup\\Description</span></span>                | <span data-ttu-id="b79c2-560">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="b79c2-560">String</span></span>      | <span data-ttu-id="b79c2-561">Binden</span><span class="sxs-lookup"><span data-stu-id="b79c2-561">Bind</span></span>   | <span data-ttu-id="b79c2-562">\@.'\$ResultGroup'.description</span><span class="sxs-lookup"><span data-stu-id="b79c2-562">\@.'\$ResultGroup'.description</span></span> |
    | <span data-ttu-id="b79c2-563">Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span><span class="sxs-lookup"><span data-stu-id="b79c2-563">Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>          | <span data-ttu-id="b79c2-564">Real-modus</span><span class="sxs-lookup"><span data-stu-id="b79c2-564">Real</span></span>        | <span data-ttu-id="b79c2-565">Binden</span><span class="sxs-lookup"><span data-stu-id="b79c2-565">Bind</span></span>   | <span data-ttu-id="b79c2-566">\@.'\$ResultGroup'.maxPoint</span><span class="sxs-lookup"><span data-stu-id="b79c2-566">\@.'\$ResultGroup'.maxPoint</span></span> |
    | <span data-ttu-id="b79c2-567">Questionnaire\\Question</span><span class="sxs-lookup"><span data-stu-id="b79c2-567">Questionnaire\\Question</span></span>                                 | <span data-ttu-id="b79c2-568">Recordlijst</span><span class="sxs-lookup"><span data-stu-id="b79c2-568">Record list</span></span> | <span data-ttu-id="b79c2-569">Binden</span><span class="sxs-lookup"><span data-stu-id="b79c2-569">Bind</span></span>   | <span data-ttu-id="b79c2-570">\@.'&lt;Relations'.KMCollectionQuestion</span><span class="sxs-lookup"><span data-stu-id="b79c2-570">\@.'&lt;Relations'.KMCollectionQuestion</span></span> |
    | <span data-ttu-id="b79c2-571">Questionnaire\\Question\\CollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="b79c2-571">Questionnaire\\Question\\CollectionSequenceNumber</span></span>       | <span data-ttu-id="b79c2-572">Geheel getal</span><span class="sxs-lookup"><span data-stu-id="b79c2-572">Integer</span></span>     | <span data-ttu-id="b79c2-573">Binden</span><span class="sxs-lookup"><span data-stu-id="b79c2-573">Bind</span></span>   | <span data-ttu-id="b79c2-574">\@.answerCollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="b79c2-574">\@.answerCollectionSequenceNumber</span></span> |
    | <span data-ttu-id="b79c2-575">Questionnaire\\Question\\Id</span><span class="sxs-lookup"><span data-stu-id="b79c2-575">Questionnaire\\Question\\Id</span></span>                             | <span data-ttu-id="b79c2-576">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="b79c2-576">String</span></span>      | <span data-ttu-id="b79c2-577">Binden</span><span class="sxs-lookup"><span data-stu-id="b79c2-577">Bind</span></span>   | <span data-ttu-id="b79c2-578">\@.kmQuestionId</span><span class="sxs-lookup"><span data-stu-id="b79c2-578">\@.kmQuestionId</span></span> |
    | <span data-ttu-id="b79c2-579">Questionnaire\\Question\\MustBeCompleted</span><span class="sxs-lookup"><span data-stu-id="b79c2-579">Questionnaire\\Question\\MustBeCompleted</span></span>                | <span data-ttu-id="b79c2-580">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="b79c2-580">String</span></span>      | <span data-ttu-id="b79c2-581">Bewerken</span><span class="sxs-lookup"><span data-stu-id="b79c2-581">Edit</span></span>   | <span data-ttu-id="b79c2-582">Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="b79c2-582">Helper.NoYesEnumToString(\@.mandatory = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="b79c2-583">Questionnaire\\Question\\PrimaryQuestion</span><span class="sxs-lookup"><span data-stu-id="b79c2-583">Questionnaire\\Question\\PrimaryQuestion</span></span>                | <span data-ttu-id="b79c2-584">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="b79c2-584">String</span></span>      | <span data-ttu-id="b79c2-585">Binden</span><span class="sxs-lookup"><span data-stu-id="b79c2-585">Bind</span></span>   | <span data-ttu-id="b79c2-586">\@.parentQuestionId</span><span class="sxs-lookup"><span data-stu-id="b79c2-586">\@.parentQuestionId</span></span> |
    | <span data-ttu-id="b79c2-587">Questionnaire\\Question\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="b79c2-587">Questionnaire\\Question\\SequenceNumber</span></span>                 | <span data-ttu-id="b79c2-588">Geheel getal</span><span class="sxs-lookup"><span data-stu-id="b79c2-588">Integer</span></span>     | <span data-ttu-id="b79c2-589">Binden</span><span class="sxs-lookup"><span data-stu-id="b79c2-589">Bind</span></span>   | <span data-ttu-id="b79c2-590">\@.SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="b79c2-590">\@.SequenceNumber</span></span> |
    | <span data-ttu-id="b79c2-591">Questionnaire\\Question\\Text</span><span class="sxs-lookup"><span data-stu-id="b79c2-591">Questionnaire\\Question\\Text</span></span>                           | <span data-ttu-id="b79c2-592">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="b79c2-592">String</span></span>      | <span data-ttu-id="b79c2-593">Binden</span><span class="sxs-lookup"><span data-stu-id="b79c2-593">Bind</span></span>   | <span data-ttu-id="b79c2-594">\@.'\$Question'.text</span><span class="sxs-lookup"><span data-stu-id="b79c2-594">\@.'\$Question'.text</span></span> |
    | <span data-ttu-id="b79c2-595">Questionnaire\\Question\\Answer</span><span class="sxs-lookup"><span data-stu-id="b79c2-595">Questionnaire\\Question\\Answer</span></span>                         | <span data-ttu-id="b79c2-596">Recordlijst</span><span class="sxs-lookup"><span data-stu-id="b79c2-596">Record list</span></span> | <span data-ttu-id="b79c2-597">Binden</span><span class="sxs-lookup"><span data-stu-id="b79c2-597">Bind</span></span>   | <span data-ttu-id="b79c2-598">\@.'\$Question'.'\$Answer'</span><span class="sxs-lookup"><span data-stu-id="b79c2-598">\@.'\$Question'.'\$Answer'</span></span> |
    | <span data-ttu-id="b79c2-599">Questionnaire\\Question\\Answer\\CorrectAnswer</span><span class="sxs-lookup"><span data-stu-id="b79c2-599">Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>          | <span data-ttu-id="b79c2-600">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="b79c2-600">String</span></span>      | <span data-ttu-id="b79c2-601">Bewerken</span><span class="sxs-lookup"><span data-stu-id="b79c2-601">Edit</span></span>   | <span data-ttu-id="b79c2-602">Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes)</span><span class="sxs-lookup"><span data-stu-id="b79c2-602">Helper.NoYesEnumToString(\@.correctAnswer = EnumAppNoYes.Yes)</span></span> |
    | <span data-ttu-id="b79c2-603">Questionnaire\\Question\\Answer\\Points</span><span class="sxs-lookup"><span data-stu-id="b79c2-603">Questionnaire\\Question\\Answer\\Points</span></span>                 | <span data-ttu-id="b79c2-604">Real-modus</span><span class="sxs-lookup"><span data-stu-id="b79c2-604">Real</span></span>        | <span data-ttu-id="b79c2-605">Binden</span><span class="sxs-lookup"><span data-stu-id="b79c2-605">Bind</span></span>   | <span data-ttu-id="b79c2-606">\@.point</span><span class="sxs-lookup"><span data-stu-id="b79c2-606">\@.point</span></span> |
    | <span data-ttu-id="b79c2-607">Questionnaire\\Question\\Answer\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="b79c2-607">Questionnaire\\Question\\Answer\\SequenceNumber</span></span>         | <span data-ttu-id="b79c2-608">Geheel getal</span><span class="sxs-lookup"><span data-stu-id="b79c2-608">Integer</span></span>     | <span data-ttu-id="b79c2-609">Binden</span><span class="sxs-lookup"><span data-stu-id="b79c2-609">Bind</span></span>   | <span data-ttu-id="b79c2-610">\@.sequenceNumber</span><span class="sxs-lookup"><span data-stu-id="b79c2-610">\@.sequenceNumber</span></span> |
    | <span data-ttu-id="b79c2-611">Questionnaire\\Question\\Answer\\Text</span><span class="sxs-lookup"><span data-stu-id="b79c2-611">Questionnaire\\Question\\Answer\\Text</span></span>                   | <span data-ttu-id="b79c2-612">Tekenreeks</span><span class="sxs-lookup"><span data-stu-id="b79c2-612">String</span></span>      | <span data-ttu-id="b79c2-613">Binden</span><span class="sxs-lookup"><span data-stu-id="b79c2-613">Bind</span></span>   | <span data-ttu-id="b79c2-614">\@.text</span><span class="sxs-lookup"><span data-stu-id="b79c2-614">\@.text</span></span> |

    <span data-ttu-id="b79c2-615">In de volgende afbeelding wordt de eindstatus van de geconfigureerde modeltoewijzing weergegeven op de pagina **Ontwerper modeltoewijzing**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-615">The following illustration shows the final state of the configured model mapping on the **Model mapping designer** page.</span></span>

    ![Volledig geconfigureerde modeltoewijzing in de ER-ontwerper voor de modeltoewijzing](./media/er-quick-start1-mapping2.png)

7. <span data-ttu-id="b79c2-617">Sla de wijzigingen op.</span><span class="sxs-lookup"><span data-stu-id="b79c2-617">Save your changes.</span></span>
8. <span data-ttu-id="b79c2-618">Sluit de pagina **Ontwerper modeltoewijzing**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-618">Close the **Model mapping designer** page.</span></span>

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping"></a><span data-ttu-id="b79c2-619">Het ontwerp van de modeltoewijzing voltooien</span><span class="sxs-lookup"><span data-stu-id="b79c2-619">Complete the design of the model mapping</span></span>

1. <span data-ttu-id="b79c2-620">Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-620">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="b79c2-621">Selecteer op de pagina **Configuraties** in de structuur met configuraties **Vragenlijsttoewijzing**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-621">On the **Configurations** page, in the configuration tree, select **Questionnaire mapping**.</span></span>
3. <span data-ttu-id="b79c2-622">Selecteer op het sneltabblad **Versies** de configuratieversie met de status **Concept**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-622">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="b79c2-623">Selecteer **Status wijzigen** \> **Voltooien**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-623">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="b79c2-624">De status van versie 1.1 van deze configuratie wordt gewijzigd van **Concept** in **Voltooid**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-624">The status of version 1.1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="b79c2-625">Versie 1.1 kan niet meer worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="b79c2-625">Version 1.1 can no longer be changed.</span></span> <span data-ttu-id="b79c2-626">Deze versie bevat de geconfigureerde modeltoewijzing en kan worden gebruikt als basis voor andere ER-configuraties.</span><span class="sxs-lookup"><span data-stu-id="b79c2-626">This version contains the configured model mapping and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="b79c2-627">Versie 1.2 van deze configuratie wordt gemaakt met de status **Concept**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-627">Version 1.2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="b79c2-628">U kunt deze versie bewerken om de configuratie **Vragenlijsttoewijzing** aan te passen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-628">You can edit this version to adjust the **Questionnaire mapping** configuration.</span></span>

![Versies van de bewerkbare ER-configuratie op de pagina Configuraties](./media/er-quick-start1-mapping-configuration.png)

> [!NOTE]
> <span data-ttu-id="b79c2-630">De geconfigureerde modeltoewijzing is uw Finance-specifieke implementatie van het abstracte gegevensmodel dat het bedrijfsdomein **Vragenlijst** vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="b79c2-630">The configured model mapping is your Finance-specific implementation of the abstract data model that represents the **Questionnaire** business domain.</span></span>

## <a name="design-a-template-for-a-custom-report"></a><a name="DesignReportTemplate"></a><span data-ttu-id="b79c2-631">Een sjabloon voor een aangepast rapport ontwerpen</span><span class="sxs-lookup"><span data-stu-id="b79c2-631">Design a template for a custom report</span></span>

<span data-ttu-id="b79c2-632">Het ER-raamwerk gebruikt vooraf gedefinieerde sjablonen om rapporten te genereren in Microsoft Office-indelingen (Excel-werkmappen of Word-documenten).</span><span class="sxs-lookup"><span data-stu-id="b79c2-632">The ER framework uses predefined templates to generate reports in Microsoft Office formats (Excel workbooks or Word documents).</span></span> <span data-ttu-id="b79c2-633">Terwijl het vereiste rapport wordt gegenereerd, wordt een sjabloon gevuld met vereiste gegevens volgens de geconfigureerde gegevensstroom.</span><span class="sxs-lookup"><span data-stu-id="b79c2-633">While the required report is being generated, a template is filled in with required data according to the configured dataflow.</span></span> <span data-ttu-id="b79c2-634">Daarom moet u eerst een sjabloon voor uw aangepaste rapport ontwerpen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-634">Therefore, you must first design a template for your custom report.</span></span> <span data-ttu-id="b79c2-635">Deze sjabloon moet zijn ontworpen als een Excel-werkmap, waarvan de structuur de indeling van een aangepast rapport vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="b79c2-635">This template must be designed as an Excel workbook, the structure of which represents the layout of a custom report.</span></span> <span data-ttu-id="b79c2-636">U moet elk Excel-item dat u wilt invullen met vereiste gegevens, een naam geven.</span><span class="sxs-lookup"><span data-stu-id="b79c2-636">You must name every Excel item that you plan to fill in with required data.</span></span>

1. <span data-ttu-id="b79c2-637">Download het bestand [Questionnaires report template.xslx](https://go.microsoft.com/fwlink/?linkid=851448) en sla het op uw lokale computer op.</span><span class="sxs-lookup"><span data-stu-id="b79c2-637">Download the [Questionnaires report template.xslx](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="b79c2-638">Open het bestand in Excel en bekijk de structuur van de werkmap.</span><span class="sxs-lookup"><span data-stu-id="b79c2-638">Open the file in Excel, and review the structure of the workbook.</span></span>

<span data-ttu-id="b79c2-639">Zoals in de volgende afbeelding wordt weergegeven, is de gedownloade sjabloon ontworpen voor het afdrukken van opgegeven vragenlijsten waarin de vragen van een vragenlijst en de juiste antwoorden worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="b79c2-639">As the following illustration shows, the downloaded template has been designed to print specified questionnaires that present a questionnaire's questions together with appropriate answers.</span></span>

![Excel-sjabloon voor het afdrukken van opgegeven vragenlijsten](./media/er-quick-start1-template-layout.png)

<span data-ttu-id="b79c2-641">Er zijn Excel-namen aan deze sjabloon toegevoegd om de details van de vragenlijst in te vullen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-641">Excel names have been added to this template to fill in the questionnaire details.</span></span> <span data-ttu-id="b79c2-642">U kunt Naambeheer gebruiken om de Excel-namen te controleren.</span><span class="sxs-lookup"><span data-stu-id="b79c2-642">You can use Name Manager to review the Excel names.</span></span>

![Naambeheer gebruiken om Excel-namen te controleren in de opgegeven Excel-sjabloon](./media/er-quick-start1-template-names.png)

<span data-ttu-id="b79c2-644">Er zijn rapportlabels toegevoegd als vaste tekst in de Engelse taal.</span><span class="sxs-lookup"><span data-stu-id="b79c2-644">Report labels have been added as fixed text in the English language.</span></span> <span data-ttu-id="b79c2-645">U kunt de rapportlabels vervangen door nieuwe Excel-namen waarmee de labels worden ingevuld met taalafhankelijke tekst door gebruik te maken van ER-opmaak[labels](#AddMmLabels) te gebruiken, zoals u ook hebt gedaan voor taalafhankelijke expressies in de geconfigureerde modeltoewijzing.</span><span class="sxs-lookup"><span data-stu-id="b79c2-645">You can replace the report labels with new Excel names that fill in the labels with language-dependent text by using the ER format [labels](#AddMmLabels), as you did for language-dependent expressions in the configured model mapping.</span></span> <span data-ttu-id="b79c2-646">In dit geval moeten ER-labels worden toegevoegd in de bewerkbare ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="b79c2-646">In this case, ER labels must be added in the editable ER format.</span></span>

<span data-ttu-id="b79c2-647">Zoals u in de volgende afbeelding kunt zien, is de aangepaste rapportkoptekst opgegeven zodat het pagineren in Excel mogelijk is.</span><span class="sxs-lookup"><span data-stu-id="b79c2-647">As the following illustration shows, the custom report header has been specified to enable Excel to do paging.</span></span>

![Aangepaste rapportkoptekst in de opgegeven Excel-sjabloon](./media/er-quick-start1-template-header.png)

## <a name="design-a-format"></a><a name="DesignFormat"></a><span data-ttu-id="b79c2-649">Een indeling ontwerpen</span><span class="sxs-lookup"><span data-stu-id="b79c2-649">Design a format</span></span>

<span data-ttu-id="b79c2-650">Als gebruiker in de rol van ER-functieconsultant moet u een nieuwe configuratie maken die een [indeling](general-electronic-reporting.md#FormatComponentOutbound)sonderdeel bevat.</span><span class="sxs-lookup"><span data-stu-id="b79c2-650">As a user in the Electronic Reporting Functional Consultant role, you must create a new ER configuration that contains a [format](general-electronic-reporting.md#FormatComponentOutbound) component.</span></span> <span data-ttu-id="b79c2-651">U moet het indelingsonderdeel configureren om op te geven hoe een rapportsjabloon tijdens runtime met vereiste gegevens wordt ingevuld.</span><span class="sxs-lookup"><span data-stu-id="b79c2-651">You must configure the format component to specify how a report template will be filled in with required data at runtime.</span></span>

<span data-ttu-id="b79c2-652">Door de stappen in de sectie [Een ontworpen indelingsconfiguratie importeren](#FormatImport) te voltooien, kunt u de vereiste indeling importeren uit het opgegeven XML-bestand.</span><span class="sxs-lookup"><span data-stu-id="b79c2-652">By completing the steps in the [Import a designed format configuration](#FormatImport) section, you can import the required format from the provided XML file.</span></span> <span data-ttu-id="b79c2-653">U kunt de stappen in de sectie [Een nieuwe indelingsconfiguratie maken](#FormatCreate) ook uitvoeren als u een helemaal nieuwe indeling wilt ontwerpen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-653">Alternatively, you can complete the steps in the [Create a new format configuration](#FormatCreate) section to design this format from scratch.</span></span>

### <a name="import-a-designed-format-configuration"></a><a name="FormatImport"></a><span data-ttu-id="b79c2-654">Een ontworpen indelingsconfiguratie importeren</span><span class="sxs-lookup"><span data-stu-id="b79c2-654">Import a designed format configuration</span></span>

1. <span data-ttu-id="b79c2-655">Download het bestand [Questionnaires format.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) en sla het op uw lokale computer op.</span><span class="sxs-lookup"><span data-stu-id="b79c2-655">Download the [Questionnaires format.version.1.1.xml](https://go.microsoft.com/fwlink/?linkid=851448) file, and save it to your local computer.</span></span>
2. <span data-ttu-id="b79c2-656">Ga naar **Organisatiebeheer** \> **Werkgebieden** \> **Elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-656">Go to **Organization administration** \> **Workspaces** \> **Electronic reporting**.</span></span>
3. <span data-ttu-id="b79c2-657">Selecteer in het werkgebied **Elektronische rapportage** de optie **Rapportconfiguraties**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-657">In the **Electronic reporting** workspace, select **Reporting configurations**.</span></span>
4. <span data-ttu-id="b79c2-658">In het actievenster selecteert u **Uitwisselen** \> **Laden uit XML-bestand**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-658">On the Action pane, Select **Exchange** \> **Load from XML file**.</span></span>
5. <span data-ttu-id="b79c2-659">Selecteer **Bladeren** en zoek en selecteer het bestand **Questionnaires format.version.1.1.xml**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-659">Select **Browse**, and then find and select the **Questionnaires format.version.1.1.xml** file.</span></span>
6. <span data-ttu-id="b79c2-660">Selecteer **OK** om de configuratie te importeren.</span><span class="sxs-lookup"><span data-stu-id="b79c2-660">Select **OK** to import the configuration.</span></span>

<span data-ttu-id="b79c2-661">Als u wilt doorgaan, gaat u naar de volgende procedure [Een nieuwe indelingsconfiguratie maken](#FormatCreate).</span><span class="sxs-lookup"><span data-stu-id="b79c2-661">To continue, skip the next procedure, [Create a new format configuration](#FormatCreate).</span></span>

### <a name="create-a-new-format-configuration"></a><a name="FormatCreate"></a><span data-ttu-id="b79c2-662">Een nieuwe indelingsconfiguratie maken</span><span class="sxs-lookup"><span data-stu-id="b79c2-662">Create a new format configuration</span></span>
 
1. <span data-ttu-id="b79c2-663">Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-663">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="b79c2-664">Selecteer op de pagina **Configuraties** in de structuur met configuraties **Vragenlijstmodel**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-664">On the **Configurations** page, in the configuration tree, select **Questionnaire model**.</span></span>
3. <span data-ttu-id="b79c2-665">Selecteer **Configuratie maken**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-665">Select **Create configuration**.</span></span>
4. <span data-ttu-id="b79c2-666">Voer de volgende stappen uit in het dialoogvenster:</span><span class="sxs-lookup"><span data-stu-id="b79c2-666">In the drop-down dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="b79c2-667">Typ in het veld **Nieuw** **Indeling gebaseerd op het gegevensmodel Questionnaires**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-667">In the **New** field, select **Format based on data model Questionnaires**.</span></span>
    2. <span data-ttu-id="b79c2-668">Voer in het veld **Naam** in **Vragenlijstrapport**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-668">In the **Name** field, enter **Questionnaire report**.</span></span>
    3. <span data-ttu-id="b79c2-669">Selecteer **1** in het veld **Versie gegevensmodel**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-669">In the **Data model version** field, select **1**.</span></span>

        > [!NOTE]
        > - <span data-ttu-id="b79c2-670">Als u een specifieke versie van het basisgegevensmodel selecteert, wordt de structuur van de bijbehorende versie van het gegevensmodel weergegeven als de structuur van de **model** gegevensbron in de indeling die wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="b79c2-670">If you select a specific version of the base data model, the structure of the corresponding version of the data model will be presented to you as the structure of the **Model** data source in the format that is created.</span></span>
        > - <span data-ttu-id="b79c2-671">U kunt dit veld leeg laten.</span><span class="sxs-lookup"><span data-stu-id="b79c2-671">You can leave this field blank.</span></span> <span data-ttu-id="b79c2-672">In dat geval wordt de structuur van de **concept** versie van het gegevensmodel weergegeven als de structuur van de **model** gegevensbron in de indeling die wordt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="b79c2-672">In that case, the structure of the **Draft** version of the data model will be presented to you as the structure of the **Model** data source in the format that is created.</span></span> <span data-ttu-id="b79c2-673">U kunt vervolgens uw model aanpassen en de aanpassingen onmiddellijk in uw indeling bekijken.</span><span class="sxs-lookup"><span data-stu-id="b79c2-673">You can then adjust your model and immediately see those adjustments in your format.</span></span> <span data-ttu-id="b79c2-674">Deze benadering kan efficiënter werken voor het onderwerp van de ER-oplossing wanneer u het gegevensmodel, de modeltoewijzing en de indeling tegelijk configureert.</span><span class="sxs-lookup"><span data-stu-id="b79c2-674">This approach might improve the efficiency of ER solution design when you configure your data model, model mapping, and format simultaneously.</span></span>
        > - <span data-ttu-id="b79c2-675">Als u een specifieke versie van het basisgegevensmodel selecteert, kunt u later overschakelen naar de **concept** versie, wanneer u begint met het bewerken van een indeling.</span><span class="sxs-lookup"><span data-stu-id="b79c2-675">If you select a specific version of the base data model, you can switch to using the **Draft** version later, when you start to edit a format.</span></span>

    4. <span data-ttu-id="b79c2-676">Selecteer in het veld **Definitie gegevensmodel** de definitie **Root**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-676">In the **Data model definition** field, select the **Root** definition.</span></span>

5. <span data-ttu-id="b79c2-677">Selecteer **Configuratie maken** om de configuratie te maken.</span><span class="sxs-lookup"><span data-stu-id="b79c2-677">Select **Create configuration** to create the configuration.</span></span>

#### <a name="import-a-report-template"></a><a name="ImportReportTemplate"></a><span data-ttu-id="b79c2-678">Een rapportsjabloon importeren</span><span class="sxs-lookup"><span data-stu-id="b79c2-678">Import a report template</span></span>

1. <span data-ttu-id="b79c2-679">Selecteer op de pagina **Configuraties** in de structuur met configuraties **Vragenlijstrapport**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-679">On the **Configurations** page, in the configuration tree, select **Questionnaire report**.</span></span>
2. <span data-ttu-id="b79c2-680">Selecteer **Ontwerper** als u een aangepaste indeling wilt configureren.</span><span class="sxs-lookup"><span data-stu-id="b79c2-680">Select **Designer** to start to configure a custom format.</span></span>
3. <span data-ttu-id="b79c2-681">Selecteer op de pagina **Indelingsontwerper** in het actievenster de optie **Importeren** \> **Importeren uit Excel**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-681">On the **Format designer** page, on the Action Pane, select **Import** \> **Import from Excel**.</span></span>
4. <span data-ttu-id="b79c2-682">Voer de volgende stappen uit in het dialoogvenster:</span><span class="sxs-lookup"><span data-stu-id="b79c2-682">In the dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="b79c2-683">Selecteer **Sjabloon toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-683">Select **Add template**.</span></span>
    2. <span data-ttu-id="b79c2-684">Zoek en selecteer het lokaal opgeslagen bestand **Questionnaires report template.xslx** en selecteer **Openen**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-684">Find and select the locally saved **Questionnaires report template.xslx** file, and then select **Open**.</span></span>
    3. <span data-ttu-id="b79c2-685">Selecteer **OK** om de sjabloon te importeren.</span><span class="sxs-lookup"><span data-stu-id="b79c2-685">Select **OK** to import the template.</span></span>

    ![Een rapportsjabloon importeren](./media/er-quick-start1-template-import.png)

<span data-ttu-id="b79c2-687">Het indelingselement **Excel\\File** wordt automatisch aan de bewerkbare indeling toegevoegd als hoofdelement.</span><span class="sxs-lookup"><span data-stu-id="b79c2-687">The **Excel\\File** format element is automatically added to the editable format as a root element.</span></span> <span data-ttu-id="b79c2-688">Bovendien wordt het indelingselement **Excel\\Range** of het indelingselement **Excel\\Cell** automatisch toegevoegd voor elke herkende Excel-naam van de geïmporteerde sjabloon.</span><span class="sxs-lookup"><span data-stu-id="b79c2-688">Additionally, either the **Excel\\Range** format element or the **Excel\\Cell** format element is automatically added for every recognized Excel name of the imported template.</span></span> <span data-ttu-id="b79c2-689">De indeling **Excel\\Header** met het geneste element **Tekenreeks** wordt automatisch toegevoegd om de koptekstinstellingen van de geïmporteerde sjabloon te weerspiegelen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-689">The **Excel\\Header** format that has the nested **String** element is automatically added to reflect the header settings of the imported template.</span></span>

![Indelingsstructuur die automatisch toegevoegde elementen bevat in de ER Operation-ontwerper](./media/er-quick-start1-template-import2.png)

#### <a name="configure-a-format"></a><a name="ConfigureFormat"></a><span data-ttu-id="b79c2-691">Een indeling configureren</span><span class="sxs-lookup"><span data-stu-id="b79c2-691">Configure a format</span></span>

1. <span data-ttu-id="b79c2-692">Selecteer op de pagina **Indelingsontwerper** in de indelingsstructuur het hoofdelement **Excel**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-692">On the **Format designer** page, in the format tree, select the **Excel** root element.</span></span>
2. <span data-ttu-id="b79c2-693">Voer op het tabblad **Indeling** aan de rechterkant van de pagina in het veld **Naam** <a name="AddFormatRootElement"></a>**Rapport** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-693">On the **Format** tab on the right side of the page, in the **Name** field, enter <a name="AddFormatRootElement"></a>**Report**.</span></span>
3. <span data-ttu-id="b79c2-694">Selecteer in het veld **Taalvoorkeur** de optie **Gebruikersvoorkeur** om het rapport uit te voeren in de voorkeurstaal van de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="b79c2-694">In the **Language preference** field, select **User preference** to run the report in the user's preferred language.</span></span>
4. <span data-ttu-id="b79c2-695">Selecteer in het veld **Cultuurvoorkeur** de optie **Gebruikersvoorkeur** om het rapport uit te voeren in de voorkeurscultuur van de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="b79c2-695">In the **Culture preference** field, select **User preference** to run the report in the user's preferred culture.</span></span>

    <span data-ttu-id="b79c2-696">Zie [Meertalige rapporten ontwerpen](er-design-multilingual-reports.md) voor informatie over het opgeven van de taal- en cultuurcontexten voor een ER-proces.</span><span class="sxs-lookup"><span data-stu-id="b79c2-696">For information about how to specify the language and culture contexts for an ER process, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

    ![Taal- en cultuurinstellingen voor het ontworpen rapport configureren in de ER Operation-ontwerper](./media/er-quick-start1-template-format-structure1.png)

5. <span data-ttu-id="b79c2-698">Vouw in de indelingsstructuur het hoofdknooppunt uit en selecteer **ResultsGroup**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-698">In the format tree, expand the root node, and then select **ResultsGroup**.</span></span>
6. <span data-ttu-id="b79c2-699">Selecteer op het tabblad **Indeling** in het veld **Replicatierichting** de optie **Geen replicatie**, omdat u niet meerdere resultaatgroepen voor één vragenlijst verwacht.</span><span class="sxs-lookup"><span data-stu-id="b79c2-699">On the **Format** tab, in the **Replication direction** field, select **No replication**, because you don't expect to have multiple result groups for a single questionnaire.</span></span>

    ![De replicatierichting definiëren voor elementen in de indeling Range van ER Operation-ontwerper](./media/er-quick-start1-template-format-structure2.png)

7. <span data-ttu-id="b79c2-701">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-701">Select **Save**.</span></span>

#### <a name="define-the-data-binding-for-a-report-title"></a><a name="DefineFormatBindings"></a><span data-ttu-id="b79c2-702">De gegevensbinding voor een rapporttitel definiëren</span><span class="sxs-lookup"><span data-stu-id="b79c2-702">Define the data binding for a report title</span></span>

<span data-ttu-id="b79c2-703">U moet een gegevensbinding opgeven voor een opmaakelement dat wordt gebruikt om de titel van een gegenereerd rapport in te vullen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-703">You must specify a data binding for a format element that is used to fill in the title of a generated report.</span></span>

1. <span data-ttu-id="b79c2-704">Selecteer op de pagina **Indelingsontwerper** op het tabblad **Toewijzing** aan de rechterkant het element **Report\\ReportTitle**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-704">On the **Format designer** page, on the **Mapping** tab on the right, select the **Report\\ReportTitle** element.</span></span>
2. <span data-ttu-id="b79c2-705">Selecteer **Formule bewerken**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-705">Select **Edit formula**.</span></span>
3. <span data-ttu-id="b79c2-706">Selecteer in de formule-editor **Vertalen**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-706">In the formula editor, select **Translate**.</span></span>
4. <span data-ttu-id="b79c2-707">Voer de volgende stappen uit in het dialoogvenster **Tekstvertaling**:</span><span class="sxs-lookup"><span data-stu-id="b79c2-707">In the **Text translation** dialog box, follow these steps:</span></span>

    1. <span data-ttu-id="b79c2-708">Voer in het veld **Label-id** **ReportTitle** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-708">In the **Label ID** field, enter **ReportTitle**.</span></span>
    2. <span data-ttu-id="b79c2-709">Voer in het veld **Tekst in standaardtaal** de tekst **Questionnaires report** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-709">In the **Text in default language** field, enter **Questionnaires report**.</span></span>
    3. <span data-ttu-id="b79c2-710">Selecteer **Vertalen** en vervolgens **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-710">Select **Translate**, and then select **Save**.</span></span>
    4. <span data-ttu-id="b79c2-711">Selecteer **Vertalen** om het dialoogvenster **Tekstvertaling** te sluiten.</span><span class="sxs-lookup"><span data-stu-id="b79c2-711">Select **Translate** to close the **Text translation** dialog box.</span></span>

5. <span data-ttu-id="b79c2-712">Sluit de Formule-editor.</span><span class="sxs-lookup"><span data-stu-id="b79c2-712">Close the formula editor.</span></span>

    ![De binding configureren om de titel van een gegenereerd rapport in te vullen](./media/er-quick-start1-add-report-title-label.png)

<span data-ttu-id="b79c2-714">Met deze techniek kunt u alle andere labels van de huidige sjabloon taalafhankelijk maken.</span><span class="sxs-lookup"><span data-stu-id="b79c2-714">You can use this technique to make all other labels of the current template language-dependent.</span></span> <span data-ttu-id="b79c2-715">Zie [Meertalige rapporten ontwerpen](er-design-multilingual-reports.md) voor informatie over hoe de toegevoegde labels van één ER-configuratie kunnen worden vertaald in alle ondersteunde talen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-715">For information about how the added labels of a single ER configuration can be translated into all supported languages, see [Design multilingual reports](er-design-multilingual-reports.md).</span></span>

#### <a name="review-model-data-source"></a><a name="ReviewModelDataSource"></a><span data-ttu-id="b79c2-716">De gegevensbron van het model controleren</span><span class="sxs-lookup"><span data-stu-id="b79c2-716">Review model data source</span></span>

1. <span data-ttu-id="b79c2-717">Selecteer op de pagina **Indelingsontwerper** op het tabblad **Toewijzing** de <a name="ModelDSName"></a>**model** gegevensbron die het basisgegevensmodel van deze ER-indeling vertegenwoordigt.</span><span class="sxs-lookup"><span data-stu-id="b79c2-717">On the **Format designer** page, on the **Mapping** tab, select the <a name="ModelDSName"></a>**model** data source that represents the base data model of this ER format.</span></span>
2. <span data-ttu-id="b79c2-718">Selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-718">Select **Edit**.</span></span>
3. <span data-ttu-id="b79c2-719">Controleer de gegevens in het dialoogvenster **Eigenschappen gegevensbron**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-719">Review the information in the **Data source properties** dialog box.</span></span> <span data-ttu-id="b79c2-720">Deze gegevensbron vertegenwoordigt versie 1 van het gegevensmodelonderdeel **Vragenlijsten** dat zich bevindt in de ER-configuratie **Model vragenlijst**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-720">This data source represents version 1 of the **Questionnaires** data model component that resides in the **Questionnaires model** ER configuration.</span></span>

![Eigenschappen van de modelgegevensbron in de ER Operation-ontwerper](./media/er-quick-start1-model-data-source.png)

#### <a name="bind-format-elements-to-data-source-fields"></a><a name="BindFormatElements"></a><span data-ttu-id="b79c2-722">Indelingselementen aan een gegevensbronvelden binden</span><span class="sxs-lookup"><span data-stu-id="b79c2-722">Bind format elements to data source fields</span></span>

<span data-ttu-id="b79c2-723">Als u wilt opgeven hoe een sjabloon tijdens runtime moet worden ingevuld, moet u elk indelingselement dat aan een geschikte Excel-naam is gekoppeld, binden aan één veld in de gegevensbron van deze indeling.</span><span class="sxs-lookup"><span data-stu-id="b79c2-723">To specify how a template is filled in at runtime, you must bind every format element that is associated with an appropriate Excel name to a single field of this format's data source.</span></span>

1. <span data-ttu-id="b79c2-724">Selecteer op de pagina **Indelingsontwerper** in de indelingsstructuur het indelingselement **Report\\CompanyName**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-724">On the **Format designer** page, in the format tree, select the **Report\\CompanyName** format element.</span></span>
2. <span data-ttu-id="b79c2-725">Selecteer op het tabblad **Toewijzing** het gegevensbronveld **model.CompanyName** van het type **Tekenreeks**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-725">On the **Mapping** tab, select the **model.CompanyName** data source field of the **String** type.</span></span>
3. <span data-ttu-id="b79c2-726">Selecteer **Binden** om een bedrijfsnaam in een sjabloon in te voeren.</span><span class="sxs-lookup"><span data-stu-id="b79c2-726">Select **Bind** to enter a company name in a template.</span></span>
4. <span data-ttu-id="b79c2-727">Selecteer in de indelingsstructuur het element **Report\\Questionnaire**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-727">In the format tree, select the **Report\\Questionnaire** element.</span></span>
5. <span data-ttu-id="b79c2-728">Selecteer op het tabblad **Toewijzing** het gegevensbronveld **model.Questionnaire** van het type **Recordlijst**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-728">On the **Mapping** tab, select the **model.Questionnaire** data source field of the **Record list** type.</span></span>
6. <span data-ttu-id="b79c2-729">Selecteer **Binden**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-729">Select **Bind**.</span></span>
7. <span data-ttu-id="b79c2-730">Selecteer **Details weergeven** als u meer details voor indelingselementen wilt weergeven.</span><span class="sxs-lookup"><span data-stu-id="b79c2-730">Select **Show details** to see more details for format elements.</span></span>

    <span data-ttu-id="b79c2-731">Het indelingselement voor het bereik **Vragenlijst** is geconfigureerd als verticaal gerepliceerd.</span><span class="sxs-lookup"><span data-stu-id="b79c2-731">The **Questionnaire** range format element is configured as vertically replicated.</span></span> <span data-ttu-id="b79c2-732">Wanneer het is gebonden aan een gegevensbron van het type **Recordlijst**, wordt het desbetreffende bereik **Vragenlijst** van de Excel-sjabloon herhaald voor elke record van de gebonden gegevensbron.</span><span class="sxs-lookup"><span data-stu-id="b79c2-732">When it's bound to a data source of the **Record list** type, the appropriate **Questionnaire** range of the Excel template is repeated for every record of the bound data source.</span></span>
 
    ![Het indelingselement voor het bereik Vragenlijst binden aan de betreffende Recordlijst-gegevens bronnen in de ER Operation-ontwerper](./media/er-quick-start1-bindings1.png)

    <span data-ttu-id="b79c2-734">Aangezien het bereik **Vragenlijst** van de Excel-sjabloon is gedefinieerd tussen de rijen 5 tot en met 14, worden deze rijen herhaald voor elke gerapporteerde vragenlijst.</span><span class="sxs-lookup"><span data-stu-id="b79c2-734">Because the **Questionnaire** range of the Excel template is defined between rows 5 through 14, these rows are repeated for every reported questionnaire.</span></span>

    ![Rijen in de Excel-sjabloon die in een gegenereerd rapport worden herhaald voor elke record van de Recordlijst-gegevensbronnen](./media/er-quick-start1-template-questionnaire-range.png)

8. <span data-ttu-id="b79c2-736">Configureer vergelijkbare bindingen voor de resterende indelingselementen, zoals wordt beschreven in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="b79c2-736">Configure similar bindings for the remaining format elements, as described in the following table.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b79c2-737">In deze tabel wordt voor de informatie in de kolom "Pad naar gegevensbron" aangenomen dat ER-functie voor het [relatieve pad](relative-path-data-bindings-er-models-format.md) is ingeschakeld.</span><span class="sxs-lookup"><span data-stu-id="b79c2-737">In this table, the information in the "Data source path" column assumes that the [relative path](relative-path-data-bindings-er-models-format.md) ER feature is turned on.</span></span>

    | <span data-ttu-id="b79c2-738">Pad van indelingselement</span><span class="sxs-lookup"><span data-stu-id="b79c2-738">Format element path</span></span>                                      | <span data-ttu-id="b79c2-739">Pad naar gegevensbron</span><span class="sxs-lookup"><span data-stu-id="b79c2-739">Data source path</span></span> |
    |----------------------------------------------------------|------------------|
    | <span data-ttu-id="b79c2-740">Excel\\ReportTitle</span><span class="sxs-lookup"><span data-stu-id="b79c2-740">Excel\\ReportTitle</span></span>                                       | <span data-ttu-id="b79c2-741">**\@"GER\_LABEL:ReportTitle"**</span><span class="sxs-lookup"><span data-stu-id="b79c2-741">**\@"GER\_LABEL:ReportTitle"**</span></span> |
    | <span data-ttu-id="b79c2-742">Excel\\CompanyName</span><span class="sxs-lookup"><span data-stu-id="b79c2-742">Excel\\CompanyName</span></span>                                       | <span data-ttu-id="b79c2-743">**model.CompanyName**</span><span class="sxs-lookup"><span data-stu-id="b79c2-743">**model.CompanyName**</span></span> |
    | <span data-ttu-id="b79c2-744">Excel\\Questionnaire</span><span class="sxs-lookup"><span data-stu-id="b79c2-744">Excel\\Questionnaire</span></span>                                     | <span data-ttu-id="b79c2-745">**model.Questionnaire**</span><span class="sxs-lookup"><span data-stu-id="b79c2-745">**model.Questionnaire**</span></span> |
    | <span data-ttu-id="b79c2-746">Excel\\Questionnaire\\Active</span><span class="sxs-lookup"><span data-stu-id="b79c2-746">Excel\\Questionnaire\\Active</span></span>                             | <span data-ttu-id="b79c2-747">**\@.Active**, waar **\@** is **model.Questionnaire**</span><span class="sxs-lookup"><span data-stu-id="b79c2-747">**\@.Active**, where **\@** is **model.Questionnaire**</span></span> |
    | <span data-ttu-id="b79c2-748">Excel\\Questionnaire\\Code</span><span class="sxs-lookup"><span data-stu-id="b79c2-748">Excel\\Questionnaire\\Code</span></span>                               | <span data-ttu-id="b79c2-749">**\@.Code**</span><span class="sxs-lookup"><span data-stu-id="b79c2-749">**\@.Code**</span></span> |
    | <span data-ttu-id="b79c2-750">Excel\\Questionnaire\\Description</span><span class="sxs-lookup"><span data-stu-id="b79c2-750">Excel\\Questionnaire\\Description</span></span>                        | <span data-ttu-id="b79c2-751">**\@.Description**</span><span class="sxs-lookup"><span data-stu-id="b79c2-751">**\@.Description**</span></span> |
    | <span data-ttu-id="b79c2-752">Excel\\Questionnaire\\QuestionnaireType</span><span class="sxs-lookup"><span data-stu-id="b79c2-752">Excel\\Questionnaire\\QuestionnaireType</span></span>                  | <span data-ttu-id="b79c2-753">**\@.QuestionnaireType**</span><span class="sxs-lookup"><span data-stu-id="b79c2-753">**\@.QuestionnaireType**</span></span> |
    | <span data-ttu-id="b79c2-754">Excel\\Questionnaire\\QuestionOrder</span><span class="sxs-lookup"><span data-stu-id="b79c2-754">Excel\\Questionnaire\\QuestionOrder</span></span>                      | <span data-ttu-id="b79c2-755">**\@.QuestionOrder**</span><span class="sxs-lookup"><span data-stu-id="b79c2-755">**\@.QuestionOrder**</span></span> |
    | <span data-ttu-id="b79c2-756">Excel\\Questionnaire\\ResultsGroup\\Code\_</span><span class="sxs-lookup"><span data-stu-id="b79c2-756">Excel\\Questionnaire\\ResultsGroup\\Code\_</span></span>               | <span data-ttu-id="b79c2-757">**\@.ResultsGroup.Code**</span><span class="sxs-lookup"><span data-stu-id="b79c2-757">**\@.ResultsGroup.Code**</span></span> |
    | <span data-ttu-id="b79c2-758">Excel\\Questionnaire\\ResultsGroup\\Description\_</span><span class="sxs-lookup"><span data-stu-id="b79c2-758">Excel\\Questionnaire\\ResultsGroup\\Description\_</span></span>        | <span data-ttu-id="b79c2-759">**\@.ResultsGroup.Description**</span><span class="sxs-lookup"><span data-stu-id="b79c2-759">**\@.ResultsGroup.Description**</span></span> |
    | <span data-ttu-id="b79c2-760">Excel\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span><span class="sxs-lookup"><span data-stu-id="b79c2-760">Excel\\Questionnaire\\ResultsGroup\\MaxNumberOfPoints</span></span>    | <span data-ttu-id="b79c2-761">**\@.ResultsGroup.MaxNumberOfPoint**</span><span class="sxs-lookup"><span data-stu-id="b79c2-761">**\@.ResultsGroup.MaxNumberOfPoint**</span></span> |
    | <span data-ttu-id="b79c2-762">Excel\\Questionnaire\\Question</span><span class="sxs-lookup"><span data-stu-id="b79c2-762">Excel\\Questionnaire\\Question</span></span>                           | <span data-ttu-id="b79c2-763">**\@.Question**</span><span class="sxs-lookup"><span data-stu-id="b79c2-763">**\@.Question**</span></span> |
    | <span data-ttu-id="b79c2-764">Excel\\Questionnaire\\Question\\CollectionSequenceNumber</span><span class="sxs-lookup"><span data-stu-id="b79c2-764">Excel\\Questionnaire\\Question\\CollectionSequenceNumber</span></span> | <span data-ttu-id="b79c2-765">**\@.CollectionSequenceNumber**, waar **\@** is **model.Questionnaire.Question**</span><span class="sxs-lookup"><span data-stu-id="b79c2-765">**\@.CollectionSequenceNumber**, where **\@** is **model.Questionnaire.Question**</span></span> |
    | <span data-ttu-id="b79c2-766">Excel\\Questionnaire\\Question\\Id</span><span class="sxs-lookup"><span data-stu-id="b79c2-766">Excel\\Questionnaire\\Question\\Id</span></span>                       | <span data-ttu-id="b79c2-767">**\@.Id**</span><span class="sxs-lookup"><span data-stu-id="b79c2-767">**\@.Id**</span></span> |
    | <span data-ttu-id="b79c2-768">Excel\\Questionnaire\\Question\\MustBeCompleted</span><span class="sxs-lookup"><span data-stu-id="b79c2-768">Excel\\Questionnaire\\Question\\MustBeCompleted</span></span>          | <span data-ttu-id="b79c2-769">**\@.MustBeCompleted**</span><span class="sxs-lookup"><span data-stu-id="b79c2-769">**\@.MustBeCompleted**</span></span> |
    | <span data-ttu-id="b79c2-770">Excel\\Questionnaire\\Question\\PrimaryQuestion</span><span class="sxs-lookup"><span data-stu-id="b79c2-770">Excel\\Questionnaire\\Question\\PrimaryQuestion</span></span>          | <span data-ttu-id="b79c2-771">**\@.PrimaryQuestion**</span><span class="sxs-lookup"><span data-stu-id="b79c2-771">**\@.PrimaryQuestion**</span></span> |
    | <span data-ttu-id="b79c2-772">Excel\\Questionnaire\\Question\\SequenceNumber</span><span class="sxs-lookup"><span data-stu-id="b79c2-772">Excel\\Questionnaire\\Question\\SequenceNumber</span></span>           | <span data-ttu-id="b79c2-773">**\@.SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="b79c2-773">**\@.SequenceNumber**</span></span> |
    | <span data-ttu-id="b79c2-774">Excel\\Questionnaire\\Question\\Text</span><span class="sxs-lookup"><span data-stu-id="b79c2-774">Excel\\Questionnaire\\Question\\Text</span></span>                     | <span data-ttu-id="b79c2-775">**\@.Text**</span><span class="sxs-lookup"><span data-stu-id="b79c2-775">**\@.Text**</span></span> |
    | <span data-ttu-id="b79c2-776">Excel\\Questionnaire\\Question\\Answer</span><span class="sxs-lookup"><span data-stu-id="b79c2-776">Excel\\Questionnaire\\Question\\Answer</span></span>                   | <span data-ttu-id="b79c2-777">**\@.Answer**</span><span class="sxs-lookup"><span data-stu-id="b79c2-777">**\@.Answer**</span></span> |
    | <span data-ttu-id="b79c2-778">Excel\\Questionnaire\\Question\\Answer\\CorrectAnswer</span><span class="sxs-lookup"><span data-stu-id="b79c2-778">Excel\\Questionnaire\\Question\\Answer\\CorrectAnswer</span></span>    | <span data-ttu-id="b79c2-779">**\@.CorrectAnswer**, waar **\@** is **model.Questionnaire.Answer**</span><span class="sxs-lookup"><span data-stu-id="b79c2-779">**\@.CorrectAnswer**, where **\@** is **model.Questionnaire.Answer**</span></span> |
    | <span data-ttu-id="b79c2-780">Excel\\Questionnaire\\Question\\Answer\\Points</span><span class="sxs-lookup"><span data-stu-id="b79c2-780">Excel\\Questionnaire\\Question\\Answer\\Points</span></span>           | <span data-ttu-id="b79c2-781">**\@.Points**</span><span class="sxs-lookup"><span data-stu-id="b79c2-781">**\@.Points**</span></span> |
    | <span data-ttu-id="b79c2-782">Excel\\Questionnaire\\Question\\Answer\\Text</span><span class="sxs-lookup"><span data-stu-id="b79c2-782">Excel\\Questionnaire\\Question\\Answer\\Text</span></span>             | <span data-ttu-id="b79c2-783">**\@.Text**</span><span class="sxs-lookup"><span data-stu-id="b79c2-783">**\@.Text**</span></span> |

9. <span data-ttu-id="b79c2-784">Wanneer u klaar bent, selecteert u **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-784">When you've finished, select **Save**.</span></span>

<span data-ttu-id="b79c2-785">In de volgende afbeelding wordt de eindstatus van de geconfigureerde gegevensbindingen weergegeven op de pagina **Indelingsontwerper**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-785">The following illustration shows the final state of the configured data bindings on the **Format designer** page.</span></span>

![Geconfigureerde gegevensbindingen in de ER Operation-ontwerper](./media/er-quick-start1-bindings2.png)

> [!IMPORTANT]
> <span data-ttu-id="b79c2-787">De hele verzameling met opgegeven gegevensbronnen en bindingen vertegenwoordigt een opmaaktoewijzingsonderdeel van de geconfigureerde indeling.</span><span class="sxs-lookup"><span data-stu-id="b79c2-787">The whole collection of specified data sources and bindings represents a format mapping component of the configured format.</span></span> <span data-ttu-id="b79c2-788">Deze indelingstoewijzing wordt aangeroepen wanneer u de geconfigureerde indeling voor het genereren van rapporten uitvoert.</span><span class="sxs-lookup"><span data-stu-id="b79c2-788">This format mapping is called when you run the configured format for report generation.</span></span>

### <a name="run-a-designed-format-from-er"></a><a name="RunFormatFromER"></a><span data-ttu-id="b79c2-789">Een ontwerpindeling vanuit ER uitvoeren</span><span class="sxs-lookup"><span data-stu-id="b79c2-789">Run a designed format from ER</span></span>

<span data-ttu-id="b79c2-790">U kunt nu een ontworpen indeling voor testdoeleinden uitvoeren vanaf de pagina **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-790">You can now run a designed format for testing purposes from the **Configurations** page.</span></span>

1. <span data-ttu-id="b79c2-791">Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-791">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="b79c2-792">Vouw op de pagina **Configuratie** in de configuratiestructuur **Vragenlijstmodel** uit en selecteer **Vragenlijstrapport**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-792">On the **Configuration** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="b79c2-793">Selecteer **Ontwerper** voor de indelingsversie met de status **Concept**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-793">Select **Designer** for the format version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="b79c2-794">Selecteer **Uitvoeren** op de pagina **Indelingsontwerper**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-794">On the **Format designer** page, select **Run**.</span></span>
5. <span data-ttu-id="b79c2-795">Configureer in het dialoogvenster **ER-parameters** op het sneltabblad **Op te nemen records** de filteroptie zo dat alleen de vragenlijst **SBCCrsExam** wordt opgenomen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-795">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
6. <span data-ttu-id="b79c2-796">Selecteer **OK** om de filteroptie te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-796">Select **OK** to confirm the filtering option.</span></span>
7. <span data-ttu-id="b79c2-797">Selecteer **OK** om het rapport uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="b79c2-797">Select **OK** to run the report.</span></span>
8. <span data-ttu-id="b79c2-798">Controleer het gegenereerde rapport.</span><span class="sxs-lookup"><span data-stu-id="b79c2-798">Review the generated report.</span></span>

<span data-ttu-id="b79c2-799">[Standaard](electronic-reporting-destinations.md#default-behavior) wordt een gegenereerd rapport afgeleverd als een Excel-bestand dat u kunt downloaden.</span><span class="sxs-lookup"><span data-stu-id="b79c2-799">By [default](electronic-reporting-destinations.md#default-behavior), a generated report is delivered as an Excel file that you can download.</span></span> <span data-ttu-id="b79c2-800">In de volgende afbeeldingen worden twee pagina's van het gegenereerde rapport in Excel-indeling weergegeven.</span><span class="sxs-lookup"><span data-stu-id="b79c2-800">The following illustrations show two pages of the generated report in Excel format.</span></span>

![Voorbeeld van een gegenereerd rapport in Excel-indeling, pagina 1](./media/er-quick-start1-report1a.png)

![Voorbeeld van een gegenereerd rapport in Excel-indeling, pagina 2](./media/er-quick-start1-report1b.png)

## <a name="tune-a-designed-format"></a><a name="TuneFormat"></a><span data-ttu-id="b79c2-803">Een ontworpen indeling optimaliseren</span><span class="sxs-lookup"><span data-stu-id="b79c2-803">Tune a designed format</span></span>

### <a name="modify-a-format-to-change-the-name-of-a-generated-document"></a><a name="ModifyToChangeName"></a><span data-ttu-id="b79c2-804">Een opmaak wijzigen om de naam van een gegenereerd document te veranderen</span><span class="sxs-lookup"><span data-stu-id="b79c2-804">Modify a format to change the name of a generated document</span></span>

<span data-ttu-id="b79c2-805">Standaard krijgt een gegenereerd document een naam met behulp van de alias van de huidige gebruiker.</span><span class="sxs-lookup"><span data-stu-id="b79c2-805">By default, a generated document is named by using the alias of the current user.</span></span> <span data-ttu-id="b79c2-806">Als u de indeling wijzigt, kunt u dit gedrag wijzigen zodat een gegenereerd document een naam krijgt op basis van uw aangepaste logica.</span><span class="sxs-lookup"><span data-stu-id="b79c2-806">By modifying the format, you can change this behavior so that a generated document is named based on your custom logic.</span></span> <span data-ttu-id="b79c2-807">De naam van een gegenereerd document kan bijvoorbeeld zijn gebaseerd op de huidige sessiedatum en -tijd en op de titel van het rapport.</span><span class="sxs-lookup"><span data-stu-id="b79c2-807">For example, the name of a generated document can be based on the current session date and time, and on the report's title.</span></span>

1. <span data-ttu-id="b79c2-808">Ga naar de pagina **Indelingsontwerper** en selecteer het basisitem **Rapport**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-808">On the **Format designer** page, select the **Report** root item.</span></span>
2. <span data-ttu-id="b79c2-809">Selecteer op het tabblad **Toewijzing** de optie **Bestandsnaam bewerken**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-809">On the **Mapping** tab, select **Edit file name**.</span></span>
3. <span data-ttu-id="b79c2-810">Voer in het veld **Formule** **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-810">In the **Formula** field, enter **CONCATENATE (\@"GER\_LABEL:ReportTitle", " - ", DATETIMEFORMAT(SESSIONNOW(), "yyyy-MM-dd hh-mm-ss"))**.</span></span>
4. <span data-ttu-id="b79c2-811">Selecteer **Opslaan** en sluit de formule-editor.</span><span class="sxs-lookup"><span data-stu-id="b79c2-811">Select **Save**, and close the formula editor.</span></span>
5. <span data-ttu-id="b79c2-812">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-812">Select **Save**.</span></span>

### <a name="modify-a-format-to-change-the-order-of-questions"></a><a name="ModifyToOrder"></a><span data-ttu-id="b79c2-813">Een opmaak wijzigen om de volgorde van vragen te veranderen</span><span class="sxs-lookup"><span data-stu-id="b79c2-813">Modify a format to change the order of questions</span></span>

<span data-ttu-id="b79c2-814">De vragen hebben niet de juiste volgorde in een gegenereerd rapport.</span><span class="sxs-lookup"><span data-stu-id="b79c2-814">The questions aren't correctly ordered in a generated report.</span></span> <span data-ttu-id="b79c2-815">U kunt de volgorde wijzigen door de indeling te wijzigen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-815">You can change the order by modifying the format.</span></span>

1. <span data-ttu-id="b79c2-816">Ga naar de pagina **Indelingsontwerper** en selecteer het basisitem **Rapport**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-816">On the **Format designer** page, select the **Report** root item.</span></span>
2. <span data-ttu-id="b79c2-817">Vouw op het tabblad **Toewijzing** in de indelingsstructuur **Report\\Questionnaire\\Question** uit.</span><span class="sxs-lookup"><span data-stu-id="b79c2-817">On the **Mapping** tab, in the format tree, expand **Report\\Questionnaire\\Question**.</span></span>

    ![Vraagindelingselement van het type Bereik in de ER Operation-ontwerper](./media/er-quick-start1-bindings3.png)

3. <span data-ttu-id="b79c2-819">Selecteer op het tabblad **Toewijzing** de optie **model.Questionnaire**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-819">On the **Mapping** tab, select **model.Questionnaire**.</span></span>
4. <span data-ttu-id="b79c2-820">Selecteer **Toevoegen** \> **Functies\\Berekend veld**, en voer in het veld **Naam** **OrderedQuestions** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-820">Select **Add** \> **Functions\\Calculated field**, and then, in the **Name** field, enter **OrderedQuestions**.</span></span>
5. <span data-ttu-id="b79c2-821">Selecteer **Formule bewerken**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-821">Select **Edit formula**.</span></span>
6. <span data-ttu-id="b79c2-822">Voer in de formule-editor in het veld **Formule** **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)** in om de lijst met vragen van de huidige vragenlijst te ordenen op volgnummer.</span><span class="sxs-lookup"><span data-stu-id="b79c2-822">In the formula editor, in the **Formula** field, enter **ORDERBY (model.Questionnaire.Question, model.Questionnaire.Question.SequenceNumber)** to order the list of questions of the current questionnaire by the sequence order number.</span></span>
7. <span data-ttu-id="b79c2-823">Selecteer **Opslaan** en sluit de formule-editor.</span><span class="sxs-lookup"><span data-stu-id="b79c2-823">Select **Save**, and close the formula editor.</span></span>
8. <span data-ttu-id="b79c2-824">Selecteer **OK** om de invoer van een nieuw berekend veld te voltooien.</span><span class="sxs-lookup"><span data-stu-id="b79c2-824">Select **OK** to complete the entry of a new calculated field.</span></span>
9. <span data-ttu-id="b79c2-825">Selecteer op het tabblad **Toewijzing** de optie **model.Questionnaire.OrderedQuestions**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-825">On the **Mapping** tab, select **model.Questionnaire.OrderedQuestions**.</span></span>
10. <span data-ttu-id="b79c2-826">Selecteer in de indelingsstructuur **Excel\\Questionnaire\\Question**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-826">In the format tree, select **Excel\\Questionnaire\\Question**.</span></span>
11. <span data-ttu-id="b79c2-827">Selecteer **Binden** en bevestig vervolgens dat het huidige pad **model.Questionnaire.Questions** wordt vervangen door het nieuwe pad **model.Questionnaire. OrderedQuestions** pad in alle bindingen van de geneste elementen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-827">Select **Bind**, and then confirm that the current **model.Questionnaire.Questions** path is replaced by the new **model.Questionnaire.OrderedQuestions** path in all bindings of nested elements.</span></span>
12. <span data-ttu-id="b79c2-828">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-828">Select **Save**.</span></span>

![Het indelingselement Vraag binden aan de geconfigureerde gegevensbron OrderedQuestions in de ER Operation-ontwerper](./media/er-quick-start1-bindings4.png)

### <a name="run-a-modified-format-from-er"></a><a name="RunFormatFromER2"></a><span data-ttu-id="b79c2-830">Een gewijzigde indeling vanuit ER uitvoeren</span><span class="sxs-lookup"><span data-stu-id="b79c2-830">Run a modified format from ER</span></span>

<span data-ttu-id="b79c2-831">U kunt nu een aangepaste indeling voor testdoeleinden uitvoeren vanuit het ER-raamwerk.</span><span class="sxs-lookup"><span data-stu-id="b79c2-831">You can now run a modified format for testing purposes from the ER framework.</span></span>

1. <span data-ttu-id="b79c2-832">Selecteer **Uitvoeren** op de pagina **Indelingsontwerper**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-832">On the **Format designer** page, select **Run**.</span></span>
2. <span data-ttu-id="b79c2-833">Configureer in het dialoogvenster **ER-parameters** op het sneltabblad **Op te nemen records** de filteroptie zo dat alleen de vragenlijst **SBCCrsExam** wordt opgenomen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-833">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
3. <span data-ttu-id="b79c2-834">Selecteer **OK** om de filteroptie te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-834">Select **OK** to confirm the filtering option.</span></span>
4. <span data-ttu-id="b79c2-835">Selecteer **OK** om het rapport uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="b79c2-835">Select **OK** to run the report.</span></span>
5. <span data-ttu-id="b79c2-836">Controleer het gegenereerde rapport.</span><span class="sxs-lookup"><span data-stu-id="b79c2-836">Review the generated report.</span></span>

<span data-ttu-id="b79c2-837">In de volgende afbeelding ziet u een gegenereerd rapport in Excel-indeling waarin de vragen op de juiste manier zijn geordend.</span><span class="sxs-lookup"><span data-stu-id="b79c2-837">The following illustration shows a generated report in Excel format where the questions are correctly ordered.</span></span>

![Gegenereerd rapport in Excel-indeling met correct geordende vragen](./media/er-quick-start1-report2.png)

### <a name="complete-the-format-design"></a><a name="CompleteFormat"></a><span data-ttu-id="b79c2-839">Het indelingsontwerp voltooien</span><span class="sxs-lookup"><span data-stu-id="b79c2-839">Complete the format design</span></span>

1. <span data-ttu-id="b79c2-840">Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-840">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="b79c2-841">Vouw op de pagina **Configuraties** in de configuratiestructuur **Vragenlijstmodel** uit en selecteer **Vragenlijstrapport**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-841">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="b79c2-842">Selecteer op het sneltabblad **Versies** de configuratieversie met de status **Concept**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-842">On the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
4. <span data-ttu-id="b79c2-843">Selecteer **Status wijzigen** \> **Voltooien**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-843">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="b79c2-844">De status van versie 1.1 van deze configuratie wordt gewijzigd van **Concept** in **Voltooid**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-844">The status of version 1.1 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="b79c2-845">Versie 1.1 kan niet meer worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="b79c2-845">Version 1.1 can no longer be changed.</span></span> <span data-ttu-id="b79c2-846">Deze versie bevat de geconfigureerde indeling en kan worden gebruikt om het aangepaste rapport af te drukken.</span><span class="sxs-lookup"><span data-stu-id="b79c2-846">This version contains the configured format and can be used to print your custom report.</span></span> <span data-ttu-id="b79c2-847">Versie 1.2 van deze configuratie wordt gemaakt met de status **Concept**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-847">Version 1.2 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="b79c2-848">U kunt deze versie bewerken om de indeling van uw **Vragenlijst** rapport aan te passen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-848">You can edit this version to adjust the format of your **Questionnaire** report.</span></span>

![Versies van de bewerkbare ER-configuratie op de pagina Configuraties](./media/er-quick-start1-format-configuration.png)

> [!NOTE]
> <span data-ttu-id="b79c2-850">De geconfigureerde indeling is uw ontwerp van het rapport **Vragenlijst** en bevat geen relaties met de specifieke Finance-artefacten.</span><span class="sxs-lookup"><span data-stu-id="b79c2-850">The configured format is your design of the **Questionnaire** report and contains no relations to the Finance-specific artefacts.</span></span>

## <a name="develop-application-artefacts-to-call-the-designed-report"></a><a name="DevelopCustomCode"></a><span data-ttu-id="b79c2-851">Toepassingsartefacten ontwikkelen om het ontworpen rapport aan te roepen</span><span class="sxs-lookup"><span data-stu-id="b79c2-851">Develop application artefacts to call the designed report</span></span>

<span data-ttu-id="b79c2-852">Als gebruiker met de rol systeembeheerder moet u nieuwe logica ontwikkelen, zodat de geconfigureerde ER-indeling kan worden aangeroepen vanuit de gebruikersinterface van de toepassing om uw aangepaste rapport te genereren.</span><span class="sxs-lookup"><span data-stu-id="b79c2-852">As a user in the System Administrator role, you must develop new logic so that the configured ER format can be called from the application user interface (UI) to generate your custom report.</span></span> <span data-ttu-id="b79c2-853">Er is momenteel geen mogelijkheid om dit type logica te configureren.</span><span class="sxs-lookup"><span data-stu-id="b79c2-853">Currently, ER doesn't offer any capability for configuring this type of logic.</span></span> <span data-ttu-id="b79c2-854">Daarom zijn technische aanpassingen vereist.</span><span class="sxs-lookup"><span data-stu-id="b79c2-854">Therefore, some engineering work is required.</span></span> 

<span data-ttu-id="b79c2-855">Als u nieuwe logica wilt ontwikkelen, moet u een topologie implementeren die ondersteuning biedt voor continu bouwvoorzieningen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-855">To develop the new logic, you must deploy a topology that supports continuous build.</span></span> <span data-ttu-id="b79c2-856">Zie [Topologieën implementeren die ondersteuning bieden voor continue bouw- en testautomatisering](../perf-test/continuous-build-test-automation.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="b79c2-856">For more information, see [Deploy topologies that support continuous build and test automation](../perf-test/continuous-build-test-automation.md).</span></span> <span data-ttu-id="b79c2-857">U moet ook toegang hebben tot de ontwikkelomgeving voor deze topologie.</span><span class="sxs-lookup"><span data-stu-id="b79c2-857">You must also have access to the development environment for this topology.</span></span> <span data-ttu-id="b79c2-858">Meer informatie over de beschikbare ER-API vindt u in [API ER-raamwerk](er-apis-app73.md).</span><span class="sxs-lookup"><span data-stu-id="b79c2-858">For more information about the available ER API, see [ER framework API](er-apis-app73.md).</span></span>

### <a name="modify-source-code"></a><a name="ModifySourceCode"></a><span data-ttu-id="b79c2-859">Broncode wijzigen</span><span class="sxs-lookup"><span data-stu-id="b79c2-859">Modify source code</span></span>

#### <a name="add-a-data-contract-class"></a><a name="DataContractClass"></a><span data-ttu-id="b79c2-860">Een gegevenscontractklasse toevoegen</span><span class="sxs-lookup"><span data-stu-id="b79c2-860">Add a data contract class</span></span>

<span data-ttu-id="b79c2-861">Voeg de nieuwe klasse **QuestionnairesErReportContract** toe aan uw Microsoft Visual Studio-project en schrijf de code waarin wordt aangegeven welk gegevenscontract moet worden gebruikt om de geconfigureerde ER-indeling uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="b79c2-861">Add the new **QuestionnairesErReportContract** class to your Microsoft Visual Studio project, and write code that specifies the data contract that should be used to run the configured ER format.</span></span>

```xpp
/// <summary>
///     This class is the data contract class for the <c>QuestionnairesErReportDP</c> class.
/// </summary>
/// <remarks>
///    This is the data contract class for the Questionnaires ER report.
/// </remarks>
[
    DataContractAttribute,
    SysOperationContractProcessingAttribute(classStr(QuestionnairesErReportUIBuilder))
    ]
    public class QuestionnairesErReportContract extends ERFormatMappingRunBaseContract implements SysOperationValidatable
{
    ERFormatMappingId formatMapping;

    /// <summary>
    ///    Validates the report parameters.
    /// </summary>
    /// <returns>
    ///    true if no errors; otherwise, false.
    /// </returns>
    public boolean validate()
    {
        boolean ret = true;
        if (!formatMapping)
        {
            ret = checkFailed(strFmt("@SYS26332", new SysDictType(extendedTypeNum(ERFormatMappingId)).label()));
        }
        return ret;
    }
    [
        DataMemberAttribute('FormatMapping'),
        SysOperationLabelAttribute(literalstr("@ElectronicReporting:FormatMapping")),
        SysOperationHelpTextAttribute(literalstr("@ElectronicReporting:FormatMapping"))
    ]
    public ERFormatMappingId parmFormatMapping(ERFormatMappingId _formatMapping = formatMapping)
    {
        formatMapping = _formatMapping;
        return formatMapping;
    }
}
```

#### <a name="add-a-ui-builder-class"></a><a name="UIBuilderClass"></a><span data-ttu-id="b79c2-862">Een UI Builder-klasse toevoegen</span><span class="sxs-lookup"><span data-stu-id="b79c2-862">Add a UI builder class</span></span>

<span data-ttu-id="b79c2-863">Voeg de nieuwe klasse **QuestionnairesErReportUIBuilder** toe aan uw Visual Studio-project en schrijf code om een runtime-dialoogvenster te genereren waarin wordt gezocht naar de indelingstoewijzings-id van de ER-indeling die moet worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="b79c2-863">Add the new **QuestionnairesErReportUIBuilder** class to your Visual Studio project, and write code to generate a runtime dialog box that will be used to look up the format mapping ID of the ER format that must be run.</span></span> <span data-ttu-id="b79c2-864">Met de opgegeven code wordt alleen gezocht naar ER-indelingen die een gegevensbron bevatten van het type **gegevensmodel** dat verwijst naar het gegevensmodel **[Vragenlijsten](#DataModeName)** met behulp van de **[basis](#RootDefinitionName)** definitie.</span><span class="sxs-lookup"><span data-stu-id="b79c2-864">The provided code looks up only ER formats that contain a data source of the **Data model** type that refers to the **[Questionnaires](#DataModeName)** data model by using the **[Root](#RootDefinitionName)** definition.</span></span>

> [!NOTE]
> <span data-ttu-id="b79c2-865">U kunt ook ER-integratiepunten gebruiken om ER-indelingen te filteren.</span><span class="sxs-lookup"><span data-stu-id="b79c2-865">Alternatively, you can use ER integration points to filter ER formats.</span></span> <span data-ttu-id="b79c2-866">Zie [API voor het weergeven van een zoekactie voor indelingstoewijzingen](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="b79c2-866">For more information, see [API to show a format mapping lookup](er-apis-app10-0-11.md#api-to-show-a-format-mapping-lookup).</span></span>

```xpp
/// <summary>
/// The UIBuilder class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportUIBuilder extends SysOperationAutomaticUIBuilder
{
    public const str ERQuestionnairesModel = 'Questionnaires';
    public const str ERQuestionnairesDataContainer = 'Root';

    /// <summary>
    /// Action after build of the dialog UI.
    /// </summary>
    public void postBuild()
    {
        DialogField formatMapping;
        super();
        formatMapping = this.bindInfo().getDialogField(this.dataContractObject(),
            methodStr(QuestionnairesErReportContract, parmFormatMapping));
        formatMapping.registerOverrideMethod(
            methodStr(FormReferenceControl, lookupReference),
            methodStr(QuestionnairesErReportUIBuilder, formatMappingLookup),
            this);
    }

    /// <summary>
    /// Performs the lookup form for format mapping.
    /// </summary>
    /// <param name="_referenceGroupControl">
    /// The control to perform lookup form.
    /// </param>
    public void formatMappingLookup(FormReferenceControl _referenceGroupControl)
    {
        ERObjectsFactory::createFormatMappingTableLookupForControlAndModel(
            _referenceGroupControl,
            ERQuestionnairesModel,
            ERQuestionnairesDataContainer).performFormLookup();
    }
}
```

#### <a name="add-a-data-provider-class"></a><a name="DataProviderClass"></a><span data-ttu-id="b79c2-867">Een gegevensproviderklasse toevoegen</span><span class="sxs-lookup"><span data-stu-id="b79c2-867">Add a data provider class</span></span>

<span data-ttu-id="b79c2-868">Voeg de nieuwe klasse **QuestionnairesErReportDP** toe aan uw Microsoft Visual Studio-project en schrijf de code waarin de gegevensprovider wordt aangegeven die moet worden gebruikt om de geconfigureerde ER-indeling uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="b79c2-868">Add the new **QuestionnairesErReportDP** class to your Visual Studio project, and write code that introduces the data provider that should used to run the configured ER format.</span></span> <span data-ttu-id="b79c2-869">De opgegeven code bevat alleen het gegevenscontract voor deze gegevensprovider.</span><span class="sxs-lookup"><span data-stu-id="b79c2-869">The provided code includes only the data contract for this data provider.</span></span>

```xpp
/// <summary>
/// Data provider class for Questionnaires ER report.
/// </summary>
public class QuestionnairesErReportDP
{
    QuestionnairesErReportContract contract;
    public static QuestionnairesErReportDP construct()
    {
        QuestionnairesErReportDP  dataProvider;
        dataProvider = new QuestionnairesErReportDP();
        return dataProvider;
    }
}
```

#### <a name="add-a-labels-file"></a><a name="LabelsFile"></a><span data-ttu-id="b79c2-870">Een labelbestand toevoegen</span><span class="sxs-lookup"><span data-stu-id="b79c2-870">Add a labels file</span></span>

<span data-ttu-id="b79c2-871">Voeg het nieuwe labelbestand **QuestionnairesErReportLabels\_en-US** toe aan uw Visual Studio-project en geef de volgende labels op voor nieuwe UI-resources:</span><span class="sxs-lookup"><span data-stu-id="b79c2-871">Add the new **QuestionnairesErReportLabels\_en-US** labels file to your Visual Studio project, and specify the following labels for new UI resources:</span></span>

- <span data-ttu-id="b79c2-872">Het label **\@QuestionnairesReport** voor een nieuwe menuopdracht met de volgende tekst in het Engels (en-US): **Questionnaires report (powered by ER)**</span><span class="sxs-lookup"><span data-stu-id="b79c2-872">The **\@QuestionnairesReport** label for a new menu item that contains the following text in US English (en-US): **Questionnaires report (powered by ER)**</span></span>
- <span data-ttu-id="b79c2-873">Het label **\@QuestionnairesReportBatchJobDescription** voor de titel van een batchtaak als een geselecteerde ER-indeling is gepland voor uitvoering als batchtaak</span><span class="sxs-lookup"><span data-stu-id="b79c2-873">The **\@QuestionnairesReportBatchJobDescription** label for a batch job title if a selected ER format is scheduled for execution as a batch job</span></span>

#### <a name="add-a-report-service-class"></a><a name="ServiceClass"></a><span data-ttu-id="b79c2-874">Een serviceklasse voor een rapport toevoegen</span><span class="sxs-lookup"><span data-stu-id="b79c2-874">Add a report service class</span></span>

<span data-ttu-id="b79c2-875">Voeg de nieuwe klasse **QuestionnairesErReportService** toe aan uw Visual Studio-project en schrijf code waarmee een ER-indeling wordt aangeroepen en geïdentificeerd met een indelingstoewijzings-id en waarmee een gegevenscontract als parameter wordt verstrekt.</span><span class="sxs-lookup"><span data-stu-id="b79c2-875">Add the new **QuestionnairesErReportService** class to your Visual Studio project, and write code that calls an ER format, identifies it by a format mapping ID, and provides a data contract as a parameter.</span></span>

```xpp
using Microsoft.Dynamics365.LocalizationFramework;
/// <summary>
/// The electronic reporting service class for Questionnaires ER report
/// </summary>
class QuestionnairesErReportService extends SysOperationServiceBase
{
    public const str ERModelDataSourceName = 'model';
    public const str DefaultExportedFileName = 'Questionnaires report';
    public const str ParametersDataSourceName = 'RunTimeParameters';

    /// <summary>
    /// Generates report by using Electronic reporting framework
    /// </summary>
    /// <param name = "_contract">The Questionnaires report contract</param>
    public void generateReportByGER(QuestionnairesErReportContract _contract)
    {
        ERFormatMappingId formatMappingId;
        QuestionnairesErReportDP  dataProvider;
        dataProvider = QuestionnairesErReportDP::construct();
        formatMappingId = _contract.parmFormatMapping();
        if (formatMappingId)
        {
            try
            {
                ERIModelDefinitionParamsAction parameters = new ERModelDefinitionParamsUIActionComposite()
                    .add(new ERModelDefinitionObjectParameterAction(ERModelDataSourceName, ParametersDataSourceName, _contract, true));

                // Call ER to generate the report.
                ERIFormatMappingRun formatMappingRun = ERObjectsFactory::createFormatMappingRunByFormatMappingId(formatMappingId, DefaultExportedFileName);
                if (formatMappingRun.parmShowPromptDialog(true))
                {
                    formatMappingRun.withParameter(parameters);
                    formatMappingRun.withFileDestination(_contract.getFileDestination());
                    formatMappingRun.run();
                }
            }
            catch
            {
                // An error occurred while exporting data.
                error("@SYP4861341");
            }
        }
        else
        {
            // There is no data available.
            info("@SYS300117");
        }
    }
}
```

<span data-ttu-id="b79c2-876">Wanneer u een ER-indeling moet gebruiken waarmee toepassingsgegevens worden uitgevoerd, moet u een gegevensbron van het type **gegevensmodel** configureren in de indelingstoewijzing.</span><span class="sxs-lookup"><span data-stu-id="b79c2-876">When you must use an ER format that runs application data, you must configure a data source of the **Data model** type in the format mapping.</span></span> <span data-ttu-id="b79c2-877">Deze gegevensbron verwijst naar een specifiek onderdeel van het opgegeven gegevensmodel met behulp van één basisdefinitie.</span><span class="sxs-lookup"><span data-stu-id="b79c2-877">This data source refers to a specific part of the specified data model by using a single root definition.</span></span> <span data-ttu-id="b79c2-878">Wanneer de ER-indeling wordt uitgevoerd, wordt deze gegevensbron aangeroepen om toegang te krijgen tot de bijbehorende ER-modeltoewijzing die is geconfigureerd voor een bepaald model en een bepaalde basisdefinitie.</span><span class="sxs-lookup"><span data-stu-id="b79c2-878">When the ER format is run, it calls this data source to access the appropriate ER model mapping that is configured for a given model and root definition.</span></span>

<span data-ttu-id="b79c2-879">Alle informatie die u kunt voorbereiden in de broncode en kunt opslaan als onderdeel van het gegevenscontract, kan worden door gegeven aan de uitgevoerde ER-indeling met behulp van een ER-modeltoewijzing van dit type.</span><span class="sxs-lookup"><span data-stu-id="b79c2-879">All the information that you might prepare in the source code and store as part of the data contract can be passed to the running ER format by using an ER model mapping of this type.</span></span> <span data-ttu-id="b79c2-880">In de ER-modeltoewijzing moet u een gegevensbron configureren van het **object** type dat naar de klasse **[QuestionnairesErReportContract](#DataContractClass)** verwijst.</span><span class="sxs-lookup"><span data-stu-id="b79c2-880">In the ER model mapping, you must configure a data source of the **Object** type that refers to the **[QuestionnairesErReportContract](#DataContractClass)** class.</span></span> <span data-ttu-id="b79c2-881">Als u een modeltoewijzing wilt identificeren, moet u een gegevensbron opgeven waarmee deze modeltoewijzing wordt aangeroepen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-881">To identify a model mapping, you must specify a data source that calls this model mapping.</span></span> <span data-ttu-id="b79c2-882">In de opgegeven code is deze gegevensbron opgegeven met de **ERModelDataSourceName**-constante die de waarde **[model](#ModelDSName)** bevat.</span><span class="sxs-lookup"><span data-stu-id="b79c2-882">In the provided code, this data source specified by the **ERModelDataSourceName** constant that has the **[model](#ModelDSName)** value.</span></span> <span data-ttu-id="b79c2-883">Als u wilt bepalen welke gegevensbron wordt gebruikt om het gegevenscontract in de modeltoewijzing beschikbaar te maken, moet u de naam van een gegevensbron opgeven.</span><span class="sxs-lookup"><span data-stu-id="b79c2-883">To identify which data source is used to expose the data contract in the model mapping, you must specify a data source name.</span></span> <span data-ttu-id="b79c2-884">In de opgegeven code wordt deze naam opgegeven met de constante **ParametersDataSourceName** die de waarde <a name="DataContractDSName"></a>**RunTimeParameters** bevat.</span><span class="sxs-lookup"><span data-stu-id="b79c2-884">In the provided code, this name is specified by the **ParametersDataSourceName** constant that has <a name="DataContractDSName"></a>**RunTimeParameters** value.</span></span>

> [!NOTE]
> <span data-ttu-id="b79c2-885">In een nieuwe omgeving moet u mogelijk de ER-metagegevens vernieuwen, zodat dit type klasse beschikbaar is in de ER-ontwerper voor modeltoewijzingen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-885">In a new environment, you might have to refresh the ER metadata so that this type of class is available in the ER model mapping designer.</span></span> <span data-ttu-id="b79c2-886">Zie [Raamwerk elektronische rapportage (ER) configureren](electronic-reporting-er-configure-parameters.md#frequently-asked-questions) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="b79c2-886">For more information, see [Configure the ER framework](electronic-reporting-er-configure-parameters.md#frequently-asked-questions).</span></span>

#### <a name="add-a-report-controller-class"></a><a name="ControllerClass"></a><span data-ttu-id="b79c2-887">Een controllerklasse voor een rapport toevoegen</span><span class="sxs-lookup"><span data-stu-id="b79c2-887">Add a report controller class</span></span>

<span data-ttu-id="b79c2-888">Voeg de nieuwe klasse **QuestionnairesErReportController** toe aan uw Visual Studio-project en schrijf code waarmee een ER-indeling naar wens wordt uitgevoerd in de synchrone of batchmodus, in het dialoogvenster dat wordt gebouwd op basis van de logica van de opgegeven klasse **QuestionnairesErReportUIBuilder**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-888">Add the new **QuestionnairesErReportController** class to your Visual Studio project, and write code that runs an ER format in either synchronous mode or batch mode, as you prefer, in the dialog box that is built based on the logic of the provided **QuestionnairesErReportUIBuilder** class.</span></span>

```xpp
/// <summary>
/// The controller for Questionnaires ER report
/// </summary>
class QuestionnairesErReportController extends ERFormatMappingRunBaseController
{
    /// <summary>
    /// The main entrance of the controller
    /// </summary>
    /// <param name = "args">The arguments</param>
    public static void main(Args args)
    {
        QuestionnairesErReportController operation;
        operation = new QuestionnairesErReportController(
            classStr(QuestionnairesErReportService),
            methodStr(QuestionnairesErReportService, generateReportByGER),
            SysOperationExecutionMode::Synchronous);
        operation.startOperation();
    }

    /// <summary>
    /// Gets caption of the dialog.
    /// </summary>
    /// <returns>Caption of the dialog</returns>
    public ClassDescription defaultCaption()
    {
        ClassDescription batchDescription;
        batchDescription = "Questionnaires report (powered by ER)";
        return batchDescription;
    }
}
```

#### <a name="add-a-menu-item"></a><a name="MenuItem"></a><span data-ttu-id="b79c2-889">Een menuopdracht toevoegen</span><span class="sxs-lookup"><span data-stu-id="b79c2-889">Add a menu item</span></span>

<span data-ttu-id="b79c2-890">Voeg de nieuwe menuopdracht **QuestionnairesErReport** toe aan uw Visual Studio-project.</span><span class="sxs-lookup"><span data-stu-id="b79c2-890">Add the new **QuestionnairesErReport** menu item to your Visual Studio project.</span></span> <span data-ttu-id="b79c2-891">In de eigenschap **Object** verwijst deze menuopdracht naar de klasse **QuestionnairesErReportController** en wordt deze gebruikt om een gebruikersmachtiging op te geven voor het selecteren en uitvoeren van een ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="b79c2-891">In the **Object** property, this menu item refers to the **QuestionnairesErReportController** class, and it's used to specify a user permission to select and run an ER format.</span></span> <span data-ttu-id="b79c2-892">In de eigenschap **Label** verwijst deze menuopdracht naar het label **\@QuestionnairesReport** dat u eerder hebt gemaakt, zodat de juiste tekst wordt weergegeven in de toepassings-UI.</span><span class="sxs-lookup"><span data-stu-id="b79c2-892">In the **Label** property, this menu item refers to the **\@QuestionnairesReport** label that you created earlier, so that correct text is presented in the application UI.</span></span>

#### <a name="add-a-menu-item-to-a-menu"></a><a name="Menu"></a><span data-ttu-id="b79c2-893">Een menuopdracht aan een menu toevoegen</span><span class="sxs-lookup"><span data-stu-id="b79c2-893">Add a menu item to a menu</span></span>

<span data-ttu-id="b79c2-894">Voeg het bestaande menu **KM** aan uw Visual Studio-project toe.</span><span class="sxs-lookup"><span data-stu-id="b79c2-894">Add the existing **KM** menu to your Visual Studio project.</span></span> <span data-ttu-id="b79c2-895">U moet een nieuw item **QuestionnairesErReport** van het type **Uitvoer** aan dit menu toevoegen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-895">You must add a new **QuestionnairesErReport** item of the **Output** type to this menu.</span></span> <span data-ttu-id="b79c2-896">Dit item moet verwijzen naar de menuopdracht **QuestionnairesErReport** die in de vorige sectie is beschreven.</span><span class="sxs-lookup"><span data-stu-id="b79c2-896">This item must refer to the **QuestionnairesErReport** menu item that is described in the previous section.</span></span>

#### <a name="build-a-visual-studio-project"></a><a name="BuildVSProject"></a><span data-ttu-id="b79c2-897">Een Visual Studio-project opbouwen</span><span class="sxs-lookup"><span data-stu-id="b79c2-897">Build a Visual Studio project</span></span>

<span data-ttu-id="b79c2-898">Stel uw project samen om een nieuwe menuopdracht beschikbaar te maken voor gebruikers.</span><span class="sxs-lookup"><span data-stu-id="b79c2-898">Build your project to make a new menu item available to users.</span></span>

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp"></a><span data-ttu-id="b79c2-899">Een indeling uit de toepassing uitvoeren</span><span class="sxs-lookup"><span data-stu-id="b79c2-899">Run a format from the application</span></span>

1. <span data-ttu-id="b79c2-900">Ga naar **Vragenlijst** \> **Ontwerp** \> **Questionnaires report (powered by ER)**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-900">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>

    ![De menuopdracht Questionnaires report (powered by ER) selecteren in de module Vragenlijst om de geconfigureerde ER-indeling uit te voeren](./media/er-quick-start1-application-menu-modified.png)

2. <span data-ttu-id="b79c2-902">Selecteer in het dialoogvenster **Indelingstoewijzing** **Questionnaires report**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-902">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="b79c2-903">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-903">Select **OK**.</span></span>
4. <span data-ttu-id="b79c2-904">Configureer in het dialoogvenster **ER-parameters** op het sneltabblad **Op te nemen records** de filteroptie zo dat alleen de vragenlijst **SBCCrsExam** wordt opgenomen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-904">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="b79c2-905">Selecteer **OK** om de filteroptie te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-905">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="b79c2-906">Selecteer **OK** om het rapport uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="b79c2-906">Select **OK** to run the report.</span></span>

    ![Selectiecriteria opgeven in het dialoogvenster ER-rapport](./media/er-quick-start1-report-run-dialog-page.png)

7. <span data-ttu-id="b79c2-908">Controleer het gegenereerde rapport.</span><span class="sxs-lookup"><span data-stu-id="b79c2-908">Review the generated report.</span></span>

## <a name="tune-a-designed-er-solution"></a><a name="TuneSolution"></a><span data-ttu-id="b79c2-909">Een ontworpen ER-oplossing optimaliseren</span><span class="sxs-lookup"><span data-stu-id="b79c2-909">Tune a designed ER solution</span></span>

<span data-ttu-id="b79c2-910">U kunt de geconfigureerde ER-oplossing wijzigen, zodat deze de gegevensproviderklasse gebruikt die u hebt ontwikkeld om toegang te krijgen tot de details van de actieve ER-indeling, zodat de naam van deze ER-indeling wordt ingevoerd in een gegenereerd rapport.</span><span class="sxs-lookup"><span data-stu-id="b79c2-910">You can modify the configured ER solution so that it uses the data provider class that you developed to access details of the running ER format, and so that it enters the name of this ER format in a generated report.</span></span>

### <a name="modify-a-model-mapping"></a><a name="ModifyModelMapping"></a><span data-ttu-id="b79c2-911">Een modeltoewijzing wijzigen</span><span class="sxs-lookup"><span data-stu-id="b79c2-911">Modify a model mapping</span></span>

#### <a name="add-data-sources-to-access-a-data-contract-object"></a><a name="AddDataSource1"></a><span data-ttu-id="b79c2-912">Gegevensbronnen toevoegen voor toegang tot een gegevenscontractobject</span><span class="sxs-lookup"><span data-stu-id="b79c2-912">Add data sources to access a data contract object</span></span>

1. <span data-ttu-id="b79c2-913">Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-913">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="b79c2-914">Vouw op de pagina **Configuraties** in de configuratiestructuur **Vragenlijstmodel** uit en selecteer **Vragenlijsttoewijzing**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-914">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire mapping**.</span></span>
3. <span data-ttu-id="b79c2-915">Selecteer **Ontwerper** om de pagina **Model aan gegevensbrontoewijzing** te openen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-915">Select **Designer** to open the **Model to datasource mapping** page.</span></span>
4. <span data-ttu-id="b79c2-916">Selecteer **Ontwerper** om de geselecteerde toewijzing in de modeltoewijzingsontwerper te openen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-916">Select **Designer** to open the selected mapping in the model mapping designer.</span></span>
5. <span data-ttu-id="b79c2-917">Selecteer op de pagina **Ontwerper modeltoewijzing** in het deelvenster **Typen gegevensbronnen** **Dynamics 365 for Operations\\Object**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-917">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Object**.</span></span>
6. <span data-ttu-id="b79c2-918">Selecteer **Basis toevoegen** in het deelvenster **Gegevensbronnen**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-918">In the **Data sources** pane, select **Add root**.</span></span>
7. <span data-ttu-id="b79c2-919">Voer in het dialoogvenster in het veld **Naam** **[RunTimeParameters](#DataContractDSName)** in, zoals wordt gedefinieerd in de broncode van de klasse **QuestionnairesErReportService**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-919">In the dialog box, in the **Name** field, enter **[RunTimeParameters](#DataContractDSName)**, as defined in the source code of the **QuestionnairesErReportService** class.</span></span>
8. <span data-ttu-id="b79c2-920">Voer in het veld **Klasse** **[QuestionnairesErReportContract](#DataContractClass)** in, die eerder is gecodeerd.</span><span class="sxs-lookup"><span data-stu-id="b79c2-920">In the **Class** field, enter **[QuestionnairesErReportContract](#DataContractClass)**, which was coded earlier.</span></span>
9. <span data-ttu-id="b79c2-921">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-921">Select **OK**.</span></span>
10. <span data-ttu-id="b79c2-922">Vouw **RunTimeParameters** uit.</span><span class="sxs-lookup"><span data-stu-id="b79c2-922">Expand **RunTimeParameters**.</span></span>

<span data-ttu-id="b79c2-923">De toegevoegde gegevensbron bevat informatie over de record-id van de actieve ER-indelingstoewijzing.</span><span class="sxs-lookup"><span data-stu-id="b79c2-923">The added data source provides information about the record ID of the running ER format mapping.</span></span>

![Gegevensbron toegevoegd aan de ontwerper voor ER-modeltoewijzingen](./media/er-quick-start1-mapping3.png)

#### <a name="add-a-data-source-to-access-er-format-mapping-records"></a><a name="AddDataSource2"></a><span data-ttu-id="b79c2-925">Een gegevensbron toevoegen voor toegang tot toewijzingsrecords met een ER-indeling</span><span class="sxs-lookup"><span data-stu-id="b79c2-925">Add a data source to access ER format mapping records</span></span>

<span data-ttu-id="b79c2-926">Ga door met het bewerken van de geselecteerde modeltoewijzing door een gegevensbron toe te voegen om toegang te krijgen tot toewijzingsrecords voor ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="b79c2-926">Continue to edit the selected model mapping by adding a data source to access ER format mapping records.</span></span>

1. <span data-ttu-id="b79c2-927">Selecteer op de pagina **Ontwerper modeltoewijzing** in het deelvenster **Typen gegevensbronnen** **Dynamics 365 for Operations\\Tabelrecords**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-927">On the **Model mapping designer** page, in the **Data source types** pane, select **Dynamics 365 for Operations\\Table records**.</span></span>
2. <span data-ttu-id="b79c2-928">Selecteer **Basis toevoegen** in het deelvenster **Gegevensbronnen**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-928">In the **Data sources** pane, select **Add root**.</span></span>
3. <span data-ttu-id="b79c2-929">Voer in het dialoogvenster in het veld **Naam** de tekst **ER1** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-929">In the dialog box, in the **Name** field, enter **ER1**.</span></span>
4. <span data-ttu-id="b79c2-930">Voer in het veld **Tabel** **ERFormatMappingTable** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-930">In the **Table** field, enter **ERFormatMappingTable**.</span></span>
5. <span data-ttu-id="b79c2-931">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-931">Select **OK**.</span></span>

#### <a name="add-a-data-source-to-access-a-format-mapping-record-of-a-running-er-format"></a><a name="AddDataSource3"></a><span data-ttu-id="b79c2-932">Een gegevensbron toevoegen voor toegang tot indelingstoewijzingsrecord van een actieve ER-indeling</span><span class="sxs-lookup"><span data-stu-id="b79c2-932">Add a data source to access a format mapping record of a running ER format</span></span>

<span data-ttu-id="b79c2-933">Ga door met het bewerken van de geselecteerde modeltoewijzing door een gegevensbron toe te voegen om toegang te krijgen tot de indelingstoewijzingsrecord van de uit te voeren ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="b79c2-933">Continue to edit the selected model mapping by adding a data source to access the format mapping record of the running ER format.</span></span>

1. <span data-ttu-id="b79c2-934">Selecteer op de pagina **Ontwerper modeltoewijzing** in het deelvenster **Typen gegevensbronnen** **Functies\\Berekend veld**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-934">On the **Model mapping designer** page, in the **Data source types** pane, select **Functions\\Calculated field**.</span></span>
2. <span data-ttu-id="b79c2-935">Selecteer **Basis toevoegen** in het deelvenster **Gegevensbronnen**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-935">In the **Data sources** pane, select **Add root**.</span></span>
3. <span data-ttu-id="b79c2-936">Voer in het dialoogvenster in het veld **Naam** de tekst **ER2** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-936">In the dialog box, in the **Name** field, enter **ER2**.</span></span>
4. <span data-ttu-id="b79c2-937">Selecteer **Formule bewerken**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-937">Select **Edit formula**.</span></span>
5. <span data-ttu-id="b79c2-938">Voer in de formule-editor in het veld **Formule** **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-938">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (FILTER(ER1, ER1.RecId = RunTimeParameters.parmFormatMapping))**.</span></span>
6. <span data-ttu-id="b79c2-939">Selecteer **Opslaan** en sluit de formule-editor.</span><span class="sxs-lookup"><span data-stu-id="b79c2-939">Select **Save**, and close the formula editor.</span></span>
7. <span data-ttu-id="b79c2-940">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-940">Select **OK**.</span></span>

#### <a name="enter-the-name-of-the-running-er-format-in-the-data-model"></a><a name="AddBinding"></a><span data-ttu-id="b79c2-941">De naam van de actieve ER-indeling in het gegevensmodel invoeren</span><span class="sxs-lookup"><span data-stu-id="b79c2-941">Enter the name of the running ER format in the data model</span></span>

<span data-ttu-id="b79c2-942">U kunt doorgaan met het bewerken van de geselecteerde modeltoewijzing, zodat de naam van de actieve ER-indeling in het gegevensmodel wordt ingevoerd.</span><span class="sxs-lookup"><span data-stu-id="b79c2-942">Continue to edit the selected model mapping so that the name of the running ER format is entered in the data model.</span></span>

1. <span data-ttu-id="b79c2-943">Vouw op de pagina **Ontwerper modeltoewijzing** in het deelvenster **Gegevensmodel** **ExecutionContext**, uit en selecteer **ExecutionContext\\FormatName**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-943">On the **Model mapping designer** page, in the **Data model** pane, expand **ExecutionContext**, and then select **ExecutionContext\\FormatName**.</span></span>
2. <span data-ttu-id="b79c2-944">Selecteer **Bewerken** in het deelvenster **Gegevensmodel** om een gegevensbinding te configureren voor het veld van het gegevensmodel.</span><span class="sxs-lookup"><span data-stu-id="b79c2-944">In the **Data model** pane, select **Edit** to configure a data binding for the selected data model's field.</span></span>
3. <span data-ttu-id="b79c2-945">Voer in de formule-editor in het veld **Formule** **FIRSTORNULL (ER2.'\>Relations'.Format).Name** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-945">In the formula editor, in the **Formula** field, enter **FIRSTORNULL (ER2.'\>Relations'.Format).Name**.</span></span>
4. <span data-ttu-id="b79c2-946">Selecteer **Opslaan** en sluit de formule-editor.</span><span class="sxs-lookup"><span data-stu-id="b79c2-946">Select **Save**, and close the formula editor.</span></span>

<span data-ttu-id="b79c2-947">Omdat u het **FormatName** hebt gebruikt, stelt de geconfigureerde modeltoewijzing nu de naam van een ER-indeling voor die deze modeltoewijzing aanroept tijdens de uitvoering.</span><span class="sxs-lookup"><span data-stu-id="b79c2-947">Because you used the **FormatName** field, the configured model mapping now exposes the name of an ER format that calls this model mapping during execution.</span></span>

![Het gegevensmodelveld binden aan de methode van de toegevoegde gegevensbron in de ontwerper van ER-modeltoewijzingen.](./media/er-quick-start1-mapping4.png)

#### <a name="complete-the-design-of-the-model-mapping"></a><a name="CompleteModelMapping2"></a><span data-ttu-id="b79c2-949">Het ontwerp van de modeltoewijzing voltooien</span><span class="sxs-lookup"><span data-stu-id="b79c2-949">Complete the design of the model mapping</span></span>

1. <span data-ttu-id="b79c2-950">Selecteer **Opslaan** op de pagina **Ontwerper modeltoewijzing**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-950">On the **Model mapping designer** page, select **Save**.</span></span>
2. <span data-ttu-id="b79c2-951">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="b79c2-951">Close the page.</span></span>
3. <span data-ttu-id="b79c2-952">Sluit de pagina Modeltoewijzingen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-952">Close the model mappings page.</span></span>
4. <span data-ttu-id="b79c2-953">Controleer op de pagina **Configuraties** in de configuratiestructuur of de configuratie van de **vragenlijsttoewijzing** nog steeds is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="b79c2-953">On the **Configurations** page, in the configuration tree, make sure that the **Questionnaire mapping** configuration is still selected.</span></span> <span data-ttu-id="b79c2-954">Selecteer vervolgens op het sneltabblad **Versies** de configuratieversie met de status **Concept**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-954">Then, on the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
5. <span data-ttu-id="b79c2-955">Selecteer **Status wijzigen** \> **Voltooien**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-955">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="b79c2-956">De status van versie 1.2 van deze configuratie wordt gewijzigd van **Concept** in **Voltooid**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-956">The status of version 1.2 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="b79c2-957">Versie 1.2 kan niet meer worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="b79c2-957">Version 1.2 can no longer be changed.</span></span> <span data-ttu-id="b79c2-958">Deze versie bevat de geconfigureerde modeltoewijzing en kan worden gebruikt als basis voor andere ER-configuraties.</span><span class="sxs-lookup"><span data-stu-id="b79c2-958">This version contains the configured model mapping and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="b79c2-959">Versie 1.3 van deze configuratie wordt gemaakt met de status **Concept**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-959">Version 1.3 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="b79c2-960">U kunt deze versie bewerken om de modeltoewijzing van de **Vragenlijst** aan te passen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-960">You can edit this version to adjust the **Questionnaire** model mapping.</span></span>

### <a name="modify-a-format"></a><a name="ModifyFormat"></a><span data-ttu-id="b79c2-961">Een indeling wijzigen</span><span class="sxs-lookup"><span data-stu-id="b79c2-961">Modify a format</span></span>

<span data-ttu-id="b79c2-962">U kunt de geconfigureerde ER-indeling wijzigen, zodat de naam wordt weergegeven in de voettekst van een rapport dat wordt gegenereerd wanneer de ER-indeling wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="b79c2-962">You can modify the configured ER format so that its name is shown in the footer of a report that is generated when the ER format is run.</span></span>

#### <a name="add-a-new-format-element"></a><a name="AddFormatElement"></a><span data-ttu-id="b79c2-963">Een nieuw opmaakelement toevoegen</span><span class="sxs-lookup"><span data-stu-id="b79c2-963">Add a new format element</span></span>

1. <span data-ttu-id="b79c2-964">Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-964">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="b79c2-965">Vouw op de pagina **Configuraties** in de configuratiestructuur **Vragenlijstmodel** uit en selecteer **Vragenlijstrapport**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-965">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="b79c2-966">Selecteer **Ontwerper**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-966">Select **Designer**.</span></span>
4. <span data-ttu-id="b79c2-967">Ga naar de pagina **Indelingsontwerper** en selecteer het basisitem **Rapport**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-967">On the **Format designer** page, select the **Report** root item.</span></span>
5. <span data-ttu-id="b79c2-968">Selecteer **Toevoegen** om een nieuw genest opmaakelement toe te voegen voor het geselecteerde hoofditem **Rapport**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-968">Select **Add** to add a new nested format element for the selected **Report** root item.</span></span>
6. <span data-ttu-id="b79c2-969">Selecteer **Excel\\Voettekst**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-969">Select **Excel\\Footer**.</span></span>
7. <span data-ttu-id="b79c2-970">Voer in het veld **Naam** de tekst **Voettekst** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-970">In the **Name** field, enter **Footer**.</span></span>
8. <span data-ttu-id="b79c2-971">Selecteer **Report\Footer** en vervolgens **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-971">Select **Report\Footer**, and then select **Add**.</span></span>
9. <span data-ttu-id="b79c2-972">Selecteer **Tekst\\Tekenreeks**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-972">Select **Text\\String**.</span></span>

#### <a name="bind-the-added-format-element"></a><a name="BindAddedFormatElement"></a><span data-ttu-id="b79c2-973">Het toegevoegde indelingselement binden</span><span class="sxs-lookup"><span data-stu-id="b79c2-973">Bind the added format element</span></span>

1. <span data-ttu-id="b79c2-974">Selecteer op de pagina **Indelingsontwerper** op het tabblad **Toewijzing** in de indelingsstructuur, **Formule bewerken** voor het actieve element **Voettekst\\Tekenreeks**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-974">On the **Format designer** page, on the **Mapping** tab, in the format tree, for the active **Footer\\String** element, select **Edit formula**.</span></span>
2. <span data-ttu-id="b79c2-975">Voer in de formule-editor in het veld **Formule** **CONCATENATE ("\&C\&10", FORMAT("Generated by'\%1' ER solution", model.ExecutionContext.FormatName))** in.</span><span class="sxs-lookup"><span data-stu-id="b79c2-975">In the formula editor, in the **Formula** field, enter **CONCATENATE ("\&C\&10", FORMAT("Generated by'\%1' ER solution", model.ExecutionContext.FormatName))**.</span></span>
3. <span data-ttu-id="b79c2-976">Selecteer **Opslaan** en sluit de formule-editor.</span><span class="sxs-lookup"><span data-stu-id="b79c2-976">Select **Save**, and close the formula editor.</span></span>
4. <span data-ttu-id="b79c2-977">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-977">Select **Save**.</span></span>

<span data-ttu-id="b79c2-978">De geconfigureerde indeling is nu gewijzigd, zodat de naam in de voettekst van een gegenereerd rapport wordt ingevoerd met het element **Voettekst\\Tekenreeks**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-978">The configured format has now been modified so that its name will be entered in the footer of a generated report by using the **Footer\\String** element.</span></span>

![Het element voor de voettekstindeling toevoegen aan de geconfigureerde indeling in de ER Operation-ontwerper](./media/er-quick-start1-template-format-structure3.png)

#### <a name="complete-the-format-design"></a><a name="CompleteFormat2"></a><span data-ttu-id="b79c2-980">Het indelingsontwerp voltooien</span><span class="sxs-lookup"><span data-stu-id="b79c2-980">Complete the format design</span></span>

1. <span data-ttu-id="b79c2-981">Sluit de pagina **Indelingsontwerper**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-981">Close the **Format designer** page.</span></span>
2. <span data-ttu-id="b79c2-982">Controleer op de pagina **Configuraties** in de configuratiestructuur of de configuratie van het **vragenlijstrappot** nog steeds is geselecteerd.</span><span class="sxs-lookup"><span data-stu-id="b79c2-982">On the **Configurations** page, in the configuration tree, make sure that the **Questionnaire report** configuration is still selected.</span></span> <span data-ttu-id="b79c2-983">Selecteer vervolgens op het sneltabblad **Versies** de configuratieversie met de status **Concept**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-983">Then, on the **Versions** FastTab, select the configuration version that has a status of **Draft**.</span></span>
3. <span data-ttu-id="b79c2-984">Selecteer **Status wijzigen** \> **Voltooien**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-984">Select **Change status** \> **Complete**.</span></span>

<span data-ttu-id="b79c2-985">De status van versie 1.2 van deze configuratie wordt gewijzigd van **Concept** in **Voltooid**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-985">The status of version 1.2 of this configuration is changed from **Draft** to **Completed**.</span></span> <span data-ttu-id="b79c2-986">Versie 1.2 kan niet meer worden gewijzigd.</span><span class="sxs-lookup"><span data-stu-id="b79c2-986">Version 1.2 can no longer be changed.</span></span> <span data-ttu-id="b79c2-987">Deze versie bevat het geconfigureerde indeling en kan worden gebruikt als basis voor andere ER-configuraties.</span><span class="sxs-lookup"><span data-stu-id="b79c2-987">This version contains the configured format and can be used as the basis for other ER configurations.</span></span> <span data-ttu-id="b79c2-988">Versie 1.3 van deze configuratie wordt gemaakt met de status **Concept**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-988">Version 1.3 of this configuration is created and has a status of **Draft**.</span></span> <span data-ttu-id="b79c2-989">U kunt deze versie bewerken om het rapport **Vragenlijst** aan te passen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-989">You can edit this version to adjust the **Questionnaire** report.</span></span>

### <a name="run-a-format-from-the-application"></a><a name="RunFormatFromApp2"></a><span data-ttu-id="b79c2-990">Een indeling uit de toepassing uitvoeren</span><span class="sxs-lookup"><span data-stu-id="b79c2-990">Run a format from the application</span></span>

1. <span data-ttu-id="b79c2-991">Ga naar **Vragenlijst** \> **Ontwerp** \> **Questionnaires report (powered by ER)**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-991">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>
2. <span data-ttu-id="b79c2-992">Selecteer in het dialoogvenster **Indelingstoewijzing** **Questionnaires report**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-992">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="b79c2-993">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-993">Select **OK**.</span></span>
4. <span data-ttu-id="b79c2-994">Configureer in het dialoogvenster **ER-parameters** op het sneltabblad **Op te nemen records** de filteroptie zo dat alleen de vragenlijst **SBCCrsExam** wordt opgenomen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-994">In the **ER parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="b79c2-995">Selecteer **OK** om de filteroptie te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-995">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="b79c2-996">Selecteer **OK** om het rapport uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="b79c2-996">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="b79c2-997">Controleer het gegenereerde rapport in de Excel-indeling.</span><span class="sxs-lookup"><span data-stu-id="b79c2-997">Review the generated report in Excel format.</span></span>

<span data-ttu-id="b79c2-998">De voettekst van het gegenereerde rapport bevat de naam van de ER-indeling die is gebruikt om het rapport te genereren.</span><span class="sxs-lookup"><span data-stu-id="b79c2-998">Notice that the footer of the generated report contains the name of the ER format that was used to generate it.</span></span>

![Gegenereerd rapport in de Excel-indeling](./media/er-quick-start1-report4.png)

### <a name="run-a-format-from-er"></a><a name="RunFormatFromER3"></a><span data-ttu-id="b79c2-1000">Een indeling vanuit ER uitvoeren</span><span class="sxs-lookup"><span data-stu-id="b79c2-1000">Run a format from ER</span></span>

1. <span data-ttu-id="b79c2-1001">Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Configuraties**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-1001">Go to **Organization administration** \> **Electronic reporting** \> **Configurations**.</span></span>
2. <span data-ttu-id="b79c2-1002">Vouw op de pagina **Configuraties** in de configuratiestructuur **Vragenlijstmodel** uit en selecteer **Vragenlijstrapport**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-1002">On the **Configurations** page, in the configuration tree, expand **Questionnaire model**, and then select **Questionnaire report**.</span></span>
3. <span data-ttu-id="b79c2-1003">Selecteer **Uitvoeren** in het actievenster.</span><span class="sxs-lookup"><span data-stu-id="b79c2-1003">On the Action Pane, select **Run**.</span></span>
4. <span data-ttu-id="b79c2-1004">Configureer in het dialoogvenster **ER-parameters** op het sneltabblad **Op te nemen records** de filteroptie zo dat alleen de vragenlijst **SBCCrsExam** wordt opgenomen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-1004">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="b79c2-1005">Selecteer **OK** om de filteroptie te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-1005">Select **OK** to confirm the filtering option.</span></span>
6. <span data-ttu-id="b79c2-1006">Selecteer **OK** om het rapport uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="b79c2-1006">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="b79c2-1007">Controleer het gegenereerde rapport in de Excel-indeling.</span><span class="sxs-lookup"><span data-stu-id="b79c2-1007">Review the generated report in Excel format.</span></span>

<span data-ttu-id="b79c2-1008">Zoals u ziet, bevat de voettekst van het gegenereerde rapport niet de naam van de ER-indeling die is gebruikt om het te genereren, omdat het gegevenscontractobject niet is doorgegeven aan de actieve modeltoewijzing toen het werd aangeroepen door de ER-indeling die vanuit ER werd uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="b79c2-1008">Notice that the footer of the generated report doesn't contain the name of ER format that was used to generate it, because the data contract object wasn't passed to the running model mapping when it was called by the ER format that was run from ER.</span></span>

### <a name="configure-a-format-destination-for-on-screen-preview"></a><a name="ConfigureDestination"></a><span data-ttu-id="b79c2-1009">Een indelingsbestemming configureren voor voorvertoning op het scherm</span><span class="sxs-lookup"><span data-stu-id="b79c2-1009">Configure a format destination for on-screen preview</span></span>

1. <span data-ttu-id="b79c2-1010">Ga naar **Organisatiebeheer** \> **Elektronische rapportage** \> **Bestemming elektronische rapportage**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-1010">Go to **Organization administration** \> **Electronic reporting** \> **Electronic reporting destination**.</span></span>
2. <span data-ttu-id="b79c2-1011">Voeg op de pagina **Bestemming elektronische rapportage** een doelrecord toe voor de geconfigureerde ER-indeling voor het **Vragenlijstrapport**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-1011">On the **Electronic reporting destination** page, add a destination record for the configured **Questionnaire report** ER format.</span></span>
3. <span data-ttu-id="b79c2-1012">Stel op het sneltabblad **Bestandsbestemming** de [bestemming](er-destination-type-screen.md) **Scherm** in voor de indelingscomponent **Rapport** die is [toegevoegd](#AddFormatRootElement) als het hoofdelement van de geconfigureerde ER-indeling voor het **vragenlijstrapport**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-1012">On the **File destination** FastTab, set up the **Screen** [destination](er-destination-type-screen.md) for the **Report** format component that has been [added](#AddFormatRootElement) as the root element of the configured **Questionnaire report** ER format.</span></span>
4. <span data-ttu-id="b79c2-1013">Configureer op het sneltabblad **Instellingen PDF-conversie** de bestemming om een rapport te converteren naar [PDF-indeling](electronic-reporting-destinations.md#OutputConversionToPDF) waarin de afdrukstand **Liggend** wordt gebruikt.</span><span class="sxs-lookup"><span data-stu-id="b79c2-1013">On the **PDF conversion settings** FastTab, configure the destination to convert a report to [PDF format](electronic-reporting-destinations.md#OutputConversionToPDF) that uses the **Landscape** page orientation.</span></span>

![De aangepaste schermbestemming configureren voor de ER-indeling op de pagina Bestemming elektronische rapportage](./media/er-quick-start1-destination.png)

### <a name="run-a-format-from-the-application-to-preview-it-as-a-pdf-document"></a><a name="RunFormatFromApp3"></a><span data-ttu-id="b79c2-1015">Een indeling van de toepassing uitvoeren voor voorvertoning als PDF-document</span><span class="sxs-lookup"><span data-stu-id="b79c2-1015">Run a format from the application to preview it as a PDF document</span></span>

1. <span data-ttu-id="b79c2-1016">Ga naar **Vragenlijst** \> **Ontwerp** \> **Questionnaires report (powered by ER)**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-1016">Go to **Questionnaire** \> **Design** \> **Questionnaires report (powered by ER)**.</span></span>
2. <span data-ttu-id="b79c2-1017">Selecteer in het dialoogvenster **Indelingstoewijzing** **Questionnaires report**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-1017">In the dialog box, in the **Format mapping** field, select **Questionnaires report**.</span></span>
3. <span data-ttu-id="b79c2-1018">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-1018">Select **OK**.</span></span>
4. <span data-ttu-id="b79c2-1019">Configureer in het dialoogvenster **ER-parameters** op het sneltabblad **Op te nemen records** de filteroptie zo dat alleen de vragenlijst **SBCCrsExam** wordt opgenomen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-1019">In the **Electronic report parameters** dialog box, on the **Records to include** FastTab, configure the filtering option so that only the **SBCCrsExam** questionnaire is included.</span></span>
5. <span data-ttu-id="b79c2-1020">Selecteer **OK** om de filteroptie te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="b79c2-1020">Select **OK** to confirm the filtering option.</span></span>

    <span data-ttu-id="b79c2-1021">Op het sneltabblad **Bestemmingen** doelen ziet u dat het veld **Uitvoer** is ingesteld op **Scherm**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-1021">On the **Destinations** FastTab, notice that the **Output** field is set to **Screen**.</span></span> <span data-ttu-id="b79c2-1022">Als u de geconfigureerde bestemming wilt wijzigen, selecteert u **Wijzigen**.</span><span class="sxs-lookup"><span data-stu-id="b79c2-1022">If you want to change the configured destination, select **Change**.</span></span>

    ![Dialoogvenster voor ER-rapport in runtime, waarin u de geconfigureerde bestemming kunt wijzigen](./media/er-quick-start1-run-settings.png)

6. <span data-ttu-id="b79c2-1024">Selecteer **OK** om het rapport uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="b79c2-1024">Select **OK** to run the report.</span></span>
7. <span data-ttu-id="b79c2-1025">Controleer het gegenereerde rapport in de PDF-indeling.</span><span class="sxs-lookup"><span data-stu-id="b79c2-1025">Review the generated report in PDF format.</span></span>

    ![Voorvertoning op het scherm van het gegenereerde rapport in PDF-indeling](./media/er-quick-start1-preview-PDF.png)

## <a name="additional-resources"></a><a name="References"></a><span data-ttu-id="b79c2-1027">Aanvullende bronnen</span><span class="sxs-lookup"><span data-stu-id="b79c2-1027">Additional resources</span></span>

- [<span data-ttu-id="b79c2-1028">Overzicht van elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="b79c2-1028">Electronic Reporting overview</span></span>](general-electronic-reporting.md)
- [<span data-ttu-id="b79c2-1029">Formuletaal in Elektronische rapportage</span><span class="sxs-lookup"><span data-stu-id="b79c2-1029">Electronic reporting formula language</span></span>](er-formula-language.md)
- [<span data-ttu-id="b79c2-1030">Meertalige rapporten ontwerpen</span><span class="sxs-lookup"><span data-stu-id="b79c2-1030">Design multilingual reports</span></span>](er-design-multilingual-reports.md)
- [<span data-ttu-id="b79c2-1031">API ER-raamwerk</span><span class="sxs-lookup"><span data-stu-id="b79c2-1031">ER framework API</span></span>](er-apis-app73.md)
- [<span data-ttu-id="b79c2-1032">CASE-functie</span><span class="sxs-lookup"><span data-stu-id="b79c2-1032">CASE function</span></span>](er-functions-logical-case.md)
- [<span data-ttu-id="b79c2-1033">CONCATENATE-functie</span><span class="sxs-lookup"><span data-stu-id="b79c2-1033">CONCATENATE function</span></span>](er-functions-text-concatenate.md)
- [<span data-ttu-id="b79c2-1034">DATETIMEFORMAT-functie</span><span class="sxs-lookup"><span data-stu-id="b79c2-1034">DATETIMEFORMAT function</span></span>](er-functions-datetime-datetimeformat.md)
- [<span data-ttu-id="b79c2-1035">FILTER-functie</span><span class="sxs-lookup"><span data-stu-id="b79c2-1035">FILTER function</span></span>](er-functions-list-filter.md)
- [<span data-ttu-id="b79c2-1036">FIRSTORNULL-functie</span><span class="sxs-lookup"><span data-stu-id="b79c2-1036">FIRSTORNULL function</span></span>](er-functions-list-firstornull.md)
- [<span data-ttu-id="b79c2-1037">FORMAT-functie</span><span class="sxs-lookup"><span data-stu-id="b79c2-1037">FORMAT function</span></span>](er-functions-text-format.md)
- [<span data-ttu-id="b79c2-1038">IF-functie</span><span class="sxs-lookup"><span data-stu-id="b79c2-1038">IF function</span></span>](er-functions-logical-if.md)
- [<span data-ttu-id="b79c2-1039">ORDERBY-functie</span><span class="sxs-lookup"><span data-stu-id="b79c2-1039">ORDERBY function</span></span>](er-functions-list-orderby.md)
- [<span data-ttu-id="b79c2-1040">SESSIONNOW-functie</span><span class="sxs-lookup"><span data-stu-id="b79c2-1040">SESSIONNOW function</span></span>](er-functions-datetime-sessionnow.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]