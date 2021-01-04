---
title: Aan de slag met de invoegtoepassing voor elektronische facturering voor Italië
description: Dit onderwerp bevat informatie waarmee u aan de slag kunt met de invoegtoepassing Elektronische facturering voor Italië in Microsoft Dynamics 365 Finance en Dynamics 365 Supply Chain Management.
author: gionoder
manager: AnnBe
ms.date: 09/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-07-08
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: c513141f820c95fe3842478361693701f1e3641b
ms.sourcegitcommit: f860ac2b18f6bbbfc4a46b497baec2477105b116
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/19/2020
ms.locfileid: "4442141"
---
# <a name="get-started-with-the-electronic-invoicing-add-on-for-italy"></a><span data-ttu-id="d4746-103">Aan de slag met de invoegtoepassing voor elektronische facturering voor Italië</span><span class="sxs-lookup"><span data-stu-id="d4746-103">Get started with the Electronic invoicing add-on for Italy</span></span>

[!include [banner](../includes/banner.md)]


> [!IMPORTANT]
> <span data-ttu-id="d4746-104">De invoegtoepassing elektronische facturering voor Italië ondersteunt momenteel mogelijk niet alle functies die beschikbaar zijn voor elektronische facturen in Microsoft Dynamics 365 Finance en Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="d4746-104">The Electronic invoicing add-on for Italy might not currently support all the functions that are available for electronic invoices in Microsoft Dynamics 365 Finance and Dynamics 365 Supply Chain Management.</span></span> 

<span data-ttu-id="d4746-105">Dit onderwerp bevat informatie waarmee u aan de slag kunt met de invoegtoepassing Elektronische facturering voor Italië.</span><span class="sxs-lookup"><span data-stu-id="d4746-105">This topic provides information that will help you get started with the Electronic invoicing add-on for Italy.</span></span> <span data-ttu-id="d4746-106">U wordt door de configuratiestappen geleid die landafhankelijk zijn in de Regulatory Configuration Services (RCS) en Finance.</span><span class="sxs-lookup"><span data-stu-id="d4746-106">It guides you through the configuration steps that are country-dependent in Regulatory Configuration Services (RCS) and Finance.</span></span> <span data-ttu-id="d4746-107">Verder wordt u door het proces voor het indienen van elektronische facturen geleid die worden gegenereerd in de Italiaanse **FatturaPA**-indeling via de service, en hierin wordt uitgelegd hoe u de resultaten van de verwerking kunt controleren.</span><span class="sxs-lookup"><span data-stu-id="d4746-107">It also guides you through the process for submitting electronic invoices that are generated in the Italy-specific **FatturaPA** format through the service, and it explains how to review the results of processing.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d4746-108">Vereisten</span><span class="sxs-lookup"><span data-stu-id="d4746-108">Prerequisites</span></span>

<span data-ttu-id="d4746-109">Voordat u de stappen in dit onderwerp uitvoert, moet u de stappen uitvoeren in [Aan de slag met de invoegtoepassing voor elektronische facturering](e-invoicing-get-started.md).</span><span class="sxs-lookup"><span data-stu-id="d4746-109">Before you complete the steps in this topic, you must complete the steps in [Get started with the Electronic invoicing add-on](e-invoicing-get-started.md).</span></span>

## <a name="rcs-setup"></a><span data-ttu-id="d4746-110">RCS-instellingen</span><span class="sxs-lookup"><span data-stu-id="d4746-110">RCS setup</span></span>

<span data-ttu-id="d4746-111">Tijdens de RCS-instelling voert u de volgende taken uit:</span><span class="sxs-lookup"><span data-stu-id="d4746-111">During the RCS setup, you will complete these tasks:</span></span>

1. <span data-ttu-id="d4746-112">Importeer de functie e-Facturering voor het exporteren van elektronische facturen van klanten in de **FatturaPA**-indeling.</span><span class="sxs-lookup"><span data-stu-id="d4746-112">Import the e-Invoicing feature for the export of customer electronic invoices in the **FatturaPA** format.</span></span>
2. <span data-ttu-id="d4746-113">Controleer de indelingsconfiguraties die nodig zijn voor het genereren, indienen en ontvangen van respons op elektronische facturen.</span><span class="sxs-lookup"><span data-stu-id="d4746-113">Review the format configurations that are required to generate, submit, and receive responses about electronic invoices.</span></span>
3. <span data-ttu-id="d4746-114">Configureer die de gebeurtenissen die scenario's voor het indienen van elektronische facturen ondersteunen.</span><span class="sxs-lookup"><span data-stu-id="d4746-114">Configure the events that support the electronic invoice submission scenarios.</span></span>
4. <span data-ttu-id="d4746-115">Publiceer de functie e-Facturering.</span><span class="sxs-lookup"><span data-stu-id="d4746-115">Publish the e-Invoicing feature.</span></span>

> [!NOTE]
> <span data-ttu-id="d4746-116">'De functie e-Facturering' is de algemene naam voor de resource die wordt geconfigureerd en gepubliceerd voor gebruik op de server van de invoegtoepassing voor elektronische facturering.</span><span class="sxs-lookup"><span data-stu-id="d4746-116">"The e-Invoicing feature" is the generic name for the resource that is configured and published to consume the Electronic invoicing add-on server.</span></span> <span data-ttu-id="d4746-117">In dit geval is het exporteren van elektronische klantfacturen de functie e-Facturering die u gaat instellen.</span><span class="sxs-lookup"><span data-stu-id="d4746-117">In this case, the export of customer electronic invoices is the e-Invoicing feature that you will set up.</span></span>

## <a name="import-the-e-invoicing-feature"></a><span data-ttu-id="d4746-118">De functie e-Facturering importeren</span><span class="sxs-lookup"><span data-stu-id="d4746-118">Import the e-Invoicing feature</span></span>

1. <span data-ttu-id="d4746-119">Meld u aan bij uw RCS-account.</span><span class="sxs-lookup"><span data-stu-id="d4746-119">Sign in to your RCS account.</span></span>
2. <span data-ttu-id="d4746-120">Selecteer in de werkruimte **Globalisatiefuncties** in de sectie **Functies** de tegel **e-Facturering**.</span><span class="sxs-lookup"><span data-stu-id="d4746-120">In the **Globalization features** workspace, in the **Features** section, select the **e-Invoicing** tile.</span></span>
3. <span data-ttu-id="d4746-121">Op de pagina **Functies voor e-Facturering** selecteert u **Importeren** om de functie e-Facturering uit de algemene opslagplaats te importeren.</span><span class="sxs-lookup"><span data-stu-id="d4746-121">On the **e-Invoicing Features** page, select **Import** to import the e-Invoicing feature from the Global repository.</span></span>

    > [!NOTE]
    > <span data-ttu-id="d4746-122">Als u de lijst met beschikbare functies niet ziet, selecteert u **Synchroniseren**.</span><span class="sxs-lookup"><span data-stu-id="d4746-122">If you don't see the list of available features, select **Synchronize**.</span></span> 

4. <span data-ttu-id="d4746-123">Selecteer de functie **E-facturen exporteren (IT)** en selecteer **Importeren**.</span><span class="sxs-lookup"><span data-stu-id="d4746-123">Select the **e-Invoices Export (IT)** feature, and then select **Import**.</span></span>

![De functie E-facturen importeren (IT) exporteren](media/e-Invoicing-services-get-started-ITA-Select-Import-e-Invoicing-feature.png)

<span data-ttu-id="d4746-125">Wanneer u de functie **E-facturen exporteren (IT)** uit de algemene opslagplaats importeert, worden alle instellingen die in de volgende secties worden beschreven, ook geïmporteerd.</span><span class="sxs-lookup"><span data-stu-id="d4746-125">When you import the **e-Invoices Export (IT)** feature from the Global repository, all the settings that are described in the next sections are also imported.</span></span>

## <a name="create-a-new-version-of-the-e-invoices-export-it-feature"></a><span data-ttu-id="d4746-126">Een nieuwe versie van de functie E-facturen exporteren (IT) maken</span><span class="sxs-lookup"><span data-stu-id="d4746-126">Create a new version of the e-Invoices Export (IT) feature</span></span>

1. <span data-ttu-id="d4746-127">Selecteer op de pagina **Functies voor e-Facturering** op het tabblad **Versies** de optie **Nieuw**.</span><span class="sxs-lookup"><span data-stu-id="d4746-127">On the **e-Invoicing Features** page, on the **Versions** tab, select **New**.</span></span> 

    ![Een nieuwe versie van de functie e-Facturering toevoegen](media/e-Invoicing-services-get-started-ITA-Select-New-e-Invoicing-feature-version.png)

    <span data-ttu-id="d4746-129">Hierna configureert u de indelingen voor elektronische rapportage (ER) die aan de functie e-Facturering zijn gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="d4746-129">Next, you will configure the Electronic reporting (ER) formats that are associated with the e-Invoicing feature.</span></span>

2. <span data-ttu-id="d4746-130">Selecteer op het tabblad **Configuraties** de optie **Toevoegen** om de configuratieversies te beheren.</span><span class="sxs-lookup"><span data-stu-id="d4746-130">On the **Configurations** tab, select **Add** to manage the configuration versions.</span></span>

    ![Configuratieversies voor de functie e-Facturering beheren](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-configurations.png)

    <span data-ttu-id="d4746-132">In deze stap voegt u de ER-indelingen toe voor verschillende bestanden die worden gebruikt voor het exporteren van Italiaanse e-facturen.</span><span class="sxs-lookup"><span data-stu-id="d4746-132">In this step, you're adding and configuring the ER formats of different files that are used to export Italian e-invoices.</span></span> <span data-ttu-id="d4746-133">Voor Italiaanse FatturaPA e-facturen gebruikt u de volgende standaardconfiguraties of de feitelijke aangepaste configuraties die u gebruikt voor e-facturering:</span><span class="sxs-lookup"><span data-stu-id="d4746-133">For Italian FatturaPA e-invoices, use either the following standard configurations or the actual customized configurations that you use for e-invoicing:</span></span>

    - <span data-ttu-id="d4746-134">Verkoopfactuur (IT)</span><span class="sxs-lookup"><span data-stu-id="d4746-134">Sales invoice (IT)</span></span>
    - <span data-ttu-id="d4746-135">Projectfactuur (IT)</span><span class="sxs-lookup"><span data-stu-id="d4746-135">Project invoice (IT)</span></span>

    <span data-ttu-id="d4746-136">Wanneer u een functie e-Facturering maakt die is afgeleid van een andere functie voor e-facturering, worden alle ER-indelingen overgenomen van de oorspronkelijke functie.</span><span class="sxs-lookup"><span data-stu-id="d4746-136">When you create an e-Invoicing feature that is derived from another e-Invoicing feature, all ER formats are inherited from the original feature.</span></span>

3. <span data-ttu-id="d4746-137">Selecteer een specifieke configuratie voor bestanden met een ER-indeling.</span><span class="sxs-lookup"><span data-stu-id="d4746-137">Select a specific ER format file configuration.</span></span>
4. <span data-ttu-id="d4746-138">Selecteer **Bewerken** of **Weergeven** om de pagina **Indelingsontwerper** te openen.</span><span class="sxs-lookup"><span data-stu-id="d4746-138">Select **Edit** or **View** to open the **Format designer** page.</span></span>

    ![De pagina Indelingsontwerper openen](media/e-Invoicing-services-get-started-ITA-Configuration-ER-format-designer.png)

5. <span data-ttu-id="d4746-140">Gebruik de pagina **Indelingsontwerper** om de configuratie van bestanden met een ER-indeling te bewerken en weer te geven.</span><span class="sxs-lookup"><span data-stu-id="d4746-140">Use the **Format designer** page to edit and view the ER format file configurations.</span></span>

    ![Pagina Indelingsontwerper](media/e-Invoicing-services-get-started-ITA-ER-format-designer.png)

## <a name="manage-the-e-invoicing-feature-setups"></a><span data-ttu-id="d4746-142">De instellingen voor de functie e-Facturering beheren</span><span class="sxs-lookup"><span data-stu-id="d4746-142">Manage the e-Invoicing feature setups</span></span>

- <span data-ttu-id="d4746-143">Selecteer op de pagina **Functies voor e-Facturering** op het tabblad **Instellingen** de optie **Toevoegen**, **Verwijderen** of **Bewerken** om de instellingen van de functie e-Facturering te beheren.</span><span class="sxs-lookup"><span data-stu-id="d4746-143">On the **e-Invoicing Features** page, on the **Setups** tab, select **Add**, **Delete**, or **Edit** to manage the e-Invoicing feature setups.</span></span>

![De instellingen voor de functie e-Facturering beheren](media/e-Invoicing-services-get-started-ITA-Manage-e-Invoicing-feature-setup.png)

<span data-ttu-id="d4746-145">In deze stap configureert u de gebeurtenissen die van toepassing zijn op elektronische facturen, waaronder het genereren van de XML-uitvoerbestanden in **FatturaPA**-indeling en digitale handtekening (indien nodig).</span><span class="sxs-lookup"><span data-stu-id="d4746-145">In this step, you configure the events that are applicable to electronic invoices, including generation of the XML output files in **FatturaPA** format and digital signing (if required).</span></span>

### <a name="configure-the-sales-invoice-feature-setup"></a><span data-ttu-id="d4746-146">De instellingen van de functie Verkoopfactuur configureren</span><span class="sxs-lookup"><span data-stu-id="d4746-146">Configure the Sales invoice feature setup</span></span>

1. <span data-ttu-id="d4746-147">Selecteer op de pagina **Functies voor e-Facturering** op het tabblad **Instellingen** in de kolom **Functie-instelling** de optie **Verkoopfactuur**.</span><span class="sxs-lookup"><span data-stu-id="d4746-147">On the **e-Invoicing Features** page, on the **Setups** tab, in the **Feature setup** column, select **Sales invoice**.</span></span>
2. <span data-ttu-id="d4746-148">Selecteer **Bewerken**.</span><span class="sxs-lookup"><span data-stu-id="d4746-148">Select **Edit**.</span></span>
3. <span data-ttu-id="d4746-149">Selecteer op de pagina **Instellingen functieversie** het tabblad **Acties** om de lijst met acties te beheren.</span><span class="sxs-lookup"><span data-stu-id="d4746-149">On the **Feature version setup** page, select the **Actions** tab to manage the list of actions.</span></span> <span data-ttu-id="d4746-150">Met acties kunt u een lijst met bewerkingen definiëren die na elkaar moeten worden uitgevoerd om de gebeurtenis volledig uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="d4746-150">Actions define a list of operations that must be run in sequential order to accomplish full execution of the event.</span></span>

    ![Tabblad Acties](media/e-Invoicing-services-get-started-ITA-Select-Actions.png)

    | <span data-ttu-id="d4746-152">Actie-ID</span><span class="sxs-lookup"><span data-stu-id="d4746-152">Action ID</span></span> | <span data-ttu-id="d4746-153">Naam actie</span><span class="sxs-lookup"><span data-stu-id="d4746-153">Action name</span></span>        | <span data-ttu-id="d4746-154">Omschrijving van de actie</span><span class="sxs-lookup"><span data-stu-id="d4746-154">Action description</span></span>                                     |
    |-----------|--------------------|--------------------------------------------------------|
    | <span data-ttu-id="d4746-155">1</span><span class="sxs-lookup"><span data-stu-id="d4746-155">1</span></span>         | <span data-ttu-id="d4746-156">Document transformeren</span><span class="sxs-lookup"><span data-stu-id="d4746-156">Transform document</span></span> | <span data-ttu-id="d4746-157">Maak het XML-bestand van de e-factuur in **FatturaPA**-indeling.</span><span class="sxs-lookup"><span data-stu-id="d4746-157">Create the e-invoice XML file in **FatturaPA** format.</span></span> |
    | <span data-ttu-id="d4746-158">2</span><span class="sxs-lookup"><span data-stu-id="d4746-158">2</span></span>         | <span data-ttu-id="d4746-159">Document ondertekenen</span><span class="sxs-lookup"><span data-stu-id="d4746-159">Sign document</span></span>      | <span data-ttu-id="d4746-160">Pas een digitale handtekening toe op het XML-bestand.</span><span class="sxs-lookup"><span data-stu-id="d4746-160">Apply a digital signature to the XML file.</span></span>             |

4. <span data-ttu-id="d4746-161">Selecteer het tabblad **Toepasbaarheidsregels** om de toepasbaarheidsregels weer te geven en te onderhouden.</span><span class="sxs-lookup"><span data-stu-id="d4746-161">Select the **Applicability rules** tab to view and maintain the applicability rules.</span></span> <span data-ttu-id="d4746-162">Regels voor toepasbaarheid definiëren de context waarin de actie wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="d4746-162">Applicability rules define the context where the action will be run.</span></span>

    ![Tabblad Toepasbaarheidsregels](media/e-Invoicing-services-get-started-ITA-Select-Applicability-rules.png)

5. <span data-ttu-id="d4746-164">Selecteer het tabblad **Variabelen** om de variabelen weer te geven en te onderhouden.</span><span class="sxs-lookup"><span data-stu-id="d4746-164">Select the **Variables** tab to view and maintain the variables.</span></span>

    ![Tabblad Variabelen](media/e-Invoicing-services-get-started-ITA-Select-Variables.png)

6. <span data-ttu-id="d4746-166">De openbare variabelen definiëren die vereist zijn om de acties uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="d4746-166">Define the public variables that are required to run the actions.</span></span>

### <a name="configure-the-project-invoice-feature-setup"></a><span data-ttu-id="d4746-167">De instellingen van de functie Projectfactuur configureren</span><span class="sxs-lookup"><span data-stu-id="d4746-167">Configure the Project invoice feature setup</span></span> 

<span data-ttu-id="d4746-168">De stappen en instellingen die nodig zijn om de instelling van de functie **Projectfactuur** te configureren, zijn vergelijkbaar met de stappen en instellingen voor de instelling van de functie **Verkoopfactuur**.</span><span class="sxs-lookup"><span data-stu-id="d4746-168">The steps and settings that are required to configure the **Project invoice** feature setup are very similar to the steps and settings for the **Sales invoice** feature setup.</span></span> <span data-ttu-id="d4746-169">Zie de procedures voor verkoopfacturen wanneer u met projectfacturen werkt.</span><span class="sxs-lookup"><span data-stu-id="d4746-169">When you work with project invoices, see the procedures for sales invoices.</span></span>

## <a name="assign-the-e-invoicing-feature-to-the-environment"></a><span data-ttu-id="d4746-170">De functie e-Facturering aan de omgeving toewijzen</span><span class="sxs-lookup"><span data-stu-id="d4746-170">Assign the e-Invoicing feature to the environment</span></span>

1. <span data-ttu-id="d4746-171">Selecteer op de pagina **Functies voor e-Facturering** op het tabblad **Omgevingen** de optie **Inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="d4746-171">On the **e-Invoicing Features** page, on the **Environments** tab, select **Enable**.</span></span>
2. <span data-ttu-id="d4746-172">Selecteer de omgeving in het veld **Omgeving**.</span><span class="sxs-lookup"><span data-stu-id="d4746-172">In the **Environment** field, select the environment.</span></span>
3. <span data-ttu-id="d4746-173">Selecteer in het veld **Geldig vanaf** de ingangsdatum van de omgeving.</span><span class="sxs-lookup"><span data-stu-id="d4746-173">In the **Effective from** field, select the date when the environment should become effective.</span></span>
4. <span data-ttu-id="d4746-174">Selecteer **Inschakelen**.</span><span class="sxs-lookup"><span data-stu-id="d4746-174">Select **Enable**.</span></span> 

![De omgeving voor e-Facturering inschakelen](media/e-Invoicing-services-get-started-ITA-Enable-e-Invoicing-environment.png)

## <a name="publish-the-e-invoicing-feature"></a><span data-ttu-id="d4746-176">De functie e-Facturering publiceren</span><span class="sxs-lookup"><span data-stu-id="d4746-176">Publish the e-invoicing feature</span></span>

<span data-ttu-id="d4746-177">U kunt de functie e-Facturering publiceren door de versiestatus te wijzigen in **Voltooid** of **Gepubliceerd**.</span><span class="sxs-lookup"><span data-stu-id="d4746-177">You can publish the e-Invoicing feature by changing the version status to **Completed** or **Published**.</span></span>

### <a name="change-the-version-status-to-completed"></a><span data-ttu-id="d4746-178">De versiestatus wijzigen in Voltooid</span><span class="sxs-lookup"><span data-stu-id="d4746-178">Change the version status to Completed</span></span>

1. <span data-ttu-id="d4746-179">Selecteer op de pagina **Functies voor e-Facturering** op het tabblad **Versies** de versie van de functie e-Facturering met de status **Concept**.</span><span class="sxs-lookup"><span data-stu-id="d4746-179">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Draft**.</span></span>
2. <span data-ttu-id="d4746-180">Selecteer **Status wijzigen \> Voltooien**.</span><span class="sxs-lookup"><span data-stu-id="d4746-180">Select **Change status \> Complete**.</span></span> 

### <a name="change-the-version-status-to-published"></a><span data-ttu-id="d4746-181">De versiestatus wijzigen in Gepubliceerd</span><span class="sxs-lookup"><span data-stu-id="d4746-181">Change the version status to Published</span></span> 

1. <span data-ttu-id="d4746-182">Selecteer op de pagina **Functies voor e-Facturering** op het tabblad **Versies** de versie van de functie e-Facturering met de status **Voltooid**.</span><span class="sxs-lookup"><span data-stu-id="d4746-182">On the **e-Invoicing Features** page, on the **Versions** tab, select the version of the e-Invoicing feature that has a status of **Completed**.</span></span>
2. <span data-ttu-id="d4746-183">Selecteer **Status wijzigen \> Publiceren**.</span><span class="sxs-lookup"><span data-stu-id="d4746-183">Select **Change status \> Publish**.</span></span>

![De status van de functie e-Facturering wijzigen](media/e-Invoicing-services-get-started-ITA-Change-status-of-e-Invoicing-feature.png)

## <a name="set-up-the-electronic-invoicing-add-on-integration-in-finance"></a><span data-ttu-id="d4746-185">De integratie van de invoegtoepassing voor elektronisch factureren instellen in Finance</span><span class="sxs-lookup"><span data-stu-id="d4746-185">Set up the Electronic invoicing add-on integration in Finance</span></span>

<span data-ttu-id="d4746-186">Tijdens de instelling van Finance voert u de volgende taken uit:</span><span class="sxs-lookup"><span data-stu-id="d4746-186">During the setup of Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="d4746-187">Het ER-gegevensmodel, de toewijzing voor het ER-gegevensmodel en de contextconfiguraties voor FatturaPA-e-facturen importeren.</span><span class="sxs-lookup"><span data-stu-id="d4746-187">Import the ER data model, the ER data model mapping, and the context configurations for FatturaPA e-invoices.</span></span>
2. <span data-ttu-id="d4746-188">Configureer het certificaat dat vereist is voor het digitaal ondertekenen van Italiaanse e-facturen.</span><span class="sxs-lookup"><span data-stu-id="d4746-188">Configure the certificate that is required to digitally sign Italian e-invoices.</span></span>

### <a name="import-the-er-data-model-data-model-mapping-and-formats"></a><span data-ttu-id="d4746-189">Het ER-gegevens model, de toewijzing van gegevensmodellen en de indelingen importeren</span><span class="sxs-lookup"><span data-stu-id="d4746-189">Import the ER data model, data model mapping, and formats</span></span>

1. <span data-ttu-id="d4746-190">Controleer in de werkruimte **Elektronische rapportage** of de configuratieaanbieder **Bedrijfsdocumentenservice** is ingesteld op **Actief**.</span><span class="sxs-lookup"><span data-stu-id="d4746-190">In the **Electronic reporting** workspace, verify that the **Business Document Service** configuration provider is set to **Active**.</span></span>
2. <span data-ttu-id="d4746-191">Selecteer **Opslagplaatsen**.</span><span class="sxs-lookup"><span data-stu-id="d4746-191">Select **Repositories**.</span></span>
3. <span data-ttu-id="d4746-192">Selecteer **Algemene resource \> Openen**.</span><span class="sxs-lookup"><span data-stu-id="d4746-192">Select **Global resource \> Open**.</span></span>
4. <span data-ttu-id="d4746-193">Importeer **Factuurmodel**, **Toewijzing factuurmodellen** en **Contextmodel klantfactuur**.</span><span class="sxs-lookup"><span data-stu-id="d4746-193">Import **Invoice model**, **Invoice model mapping**, and **Customer invoice context model**.</span></span>

#### <a name="turn-on-the-feature-for-exporting-customer-electronic-invoices-for-italy"></a><span data-ttu-id="d4746-194">De functie voor het exporteren van elektronische klantfacturen voor Italië inschakelen</span><span class="sxs-lookup"><span data-stu-id="d4746-194">Turn on the feature for exporting customer electronic invoices for Italy</span></span>

1. <span data-ttu-id="d4746-195">Ga naar **Organisatiebeheer \> Instellen \> Parameters voor elektronische documenten**.</span><span class="sxs-lookup"><span data-stu-id="d4746-195">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="d4746-196">Schakel op het tabblad **Functies** het selectievakje **Ingeschakeld** in bij de rij voor functiereferentie **IT00036**.</span><span class="sxs-lookup"><span data-stu-id="d4746-196">On the **Features** tab, select the **Enabled** check box in the row for feature reference **IT00036**.</span></span>

![De functie FatturaPA inschakelen](media/e-Invoicing-services-get-started-ITA-Enable-FatturaPA-feature.png)

#### <a name="configure-electronic-documents"></a><span data-ttu-id="d4746-198">Elektronische documenten configureren</span><span class="sxs-lookup"><span data-stu-id="d4746-198">Configure electronic documents</span></span>

1. <span data-ttu-id="d4746-199">Ga naar **Organisatiebeheer \> Instellen \> Parameters voor elektronische documenten**.</span><span class="sxs-lookup"><span data-stu-id="d4746-199">Go to **Organization administration \> Setup \> Electronic document parameters**.</span></span>
2. <span data-ttu-id="d4746-200">Selecteer op het tabblad **Elektronisch document** de optie **Toevoegen** en voer de tabellen in die vereist zijn om Italiaanse e-facturen te genereren:</span><span class="sxs-lookup"><span data-stu-id="d4746-200">On the **Electronic document** tab, select **Add**, and enter the tables that are required to generate Italian e-invoices:</span></span>

    - <span data-ttu-id="d4746-201">**Tabelnaam:** Klantfactuurjournaal</span><span class="sxs-lookup"><span data-stu-id="d4746-201">**Table name:** Customer invoice journal</span></span>
    - <span data-ttu-id="d4746-202">**Tabelnaam:** Projectfactuur</span><span class="sxs-lookup"><span data-stu-id="d4746-202">**Table name:** Project invoice</span></span>

3. <span data-ttu-id="d4746-203">Definieer voor elke tabel een gerelateerde documentcontext:</span><span class="sxs-lookup"><span data-stu-id="d4746-203">For each table, define a related document context:</span></span>

    - <span data-ttu-id="d4746-204">Selecteer voor **Klantfactuurjournaal** de optie **Klantfactuurcontext**.</span><span class="sxs-lookup"><span data-stu-id="d4746-204">For **Customer invoice journal**, select **Customer invoice context**.</span></span>
    - <span data-ttu-id="d4746-205">Selecteer voor **Projectfactuur** de optie **Projectfactuurcontext**.</span><span class="sxs-lookup"><span data-stu-id="d4746-205">For **Project invoice**, select **Project invoice context**.</span></span>

![Responstypen instellen](media/e-Invoicing-services-get-started-ITA-Set-up-response-types.png)

## <a name="electronic-invoice-processing"></a><span data-ttu-id="d4746-207">Verwerking van elektronische facturen</span><span class="sxs-lookup"><span data-stu-id="d4746-207">Electronic invoice processing</span></span>

<span data-ttu-id="d4746-208">Tijdens de verwerking in Finance voert u de volgende taken uit:</span><span class="sxs-lookup"><span data-stu-id="d4746-208">During processing in Finance, you will complete these tasks:</span></span>

1. <span data-ttu-id="d4746-209">Italiaanse e-facturen genereren via de invoegtoepassing voor elektronische facturering</span><span class="sxs-lookup"><span data-stu-id="d4746-209">Generate Italian e-invoices through the Electronic invoicing add-on</span></span>
2. <span data-ttu-id="d4746-210">De uitvoeringslogboeken weergeven en de resultaten van de verwerking beoordelen</span><span class="sxs-lookup"><span data-stu-id="d4746-210">View the execution logs and review the results of processing</span></span>

### <a name="generate-electronic-invoices"></a><span data-ttu-id="d4746-211">Elektronische facturen genereren</span><span class="sxs-lookup"><span data-stu-id="d4746-211">Generate electronic invoices</span></span>

<span data-ttu-id="d4746-212">Nadat u de functie **Integratie configureerbare invoegtoepassing voor elektronisch factureren** hebt ingeschakeld en de functie **IT00036** hebt geactiveerd, kan het oude Finance-proces voor het genereren van Italiaanse e-facturen niet meer worden gebruikt.</span><span class="sxs-lookup"><span data-stu-id="d4746-212">After you turn on the **Configurable Electronic invoicing add-on integration** feature and activate the **IT00036** feature, the old Finance process for generating Italian e-invoices can no longer be used.</span></span> <span data-ttu-id="d4746-213">Het wordt vervangen door een nieuw proces met de naam **Elektronische documenten indienen**.</span><span class="sxs-lookup"><span data-stu-id="d4746-213">It's replaced by a new process that is named **Submit electronic documents**.</span></span>

<span data-ttu-id="d4746-214">U kunt de documenten handmatig indienen op basis van uw behoefte aan e-factuurdocumenten.</span><span class="sxs-lookup"><span data-stu-id="d4746-214">You can submit the documents manually, based on your demand for e-invoice documents.</span></span>

> [!NOTE]
> <span data-ttu-id="d4746-215">Voordat u doorgaat, controleert u of de instellingen die nodig zijn voor de Italiaanse e-facturen zijn voltooid.</span><span class="sxs-lookup"><span data-stu-id="d4746-215">Before you continue, verify that the setup that is required for Italian e-invoices was completed.</span></span> <span data-ttu-id="d4746-216">Zie [Elektronische klantfacturen](https://docs.microsoft.com/dynamics365/finance/localizations/emea-ita-e-invoices) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="d4746-216">For more information, see [Customer electronic invoices](https://docs.microsoft.com/dynamics365/finance/localizations/emea-ita-e-invoices).</span></span> <span data-ttu-id="d4746-217">Houd er rekening mee dat sommige instellingsstappen die in dat onderwerp worden beschreven, mogelijk niet beschikbaar zijn vanwege de activering van elektronische facturering.</span><span class="sxs-lookup"><span data-stu-id="d4746-217">Be aware that some of the setup steps that are described in that topic might be unavailable because of Electronic invoicing add-on activation.</span></span>

1. <span data-ttu-id="d4746-218">Ga naar **Organisatiebeheer \> Periodiek \> Elektronische documenten \> Elektronische documenten indienen**.</span><span class="sxs-lookup"><span data-stu-id="d4746-218">Go to **Organization administration \> Periodic \> Electronic documents \> Submit electronic documents**.</span></span>
2. <span data-ttu-id="d4746-219">Als u een document voor het eerst indient, moet u de optie **Documenten opnieuw indienen** op **Nee** instellen.</span><span class="sxs-lookup"><span data-stu-id="d4746-219">For the first submission of any document, set the **Resubmit documents** option to **No**.</span></span> <span data-ttu-id="d4746-220">Stel deze optie in op **Ja** als u een document opnieuw moet indienen via de service.</span><span class="sxs-lookup"><span data-stu-id="d4746-220">If you must resubmit a document through the service, set this option to **Yes**.</span></span>
3. <span data-ttu-id="d4746-221">Selecteer op het sneltabblad **Op te nemen records** de optie **Filter** om het dialoogvenster **Query** te openen. Hier kunt u een query samenstellen om documenten te selecteren die u wilt indienen.</span><span class="sxs-lookup"><span data-stu-id="d4746-221">On the **Records to include** FastTab, select **Filter** to open the **Inquiry** dialog box, where you can build a query to select documents for submission.</span></span>

![Het dialoogvenster Elektronische documenten indienen](media/e-Invoicing-services-get-started-ITA-Submission-form.png)

#### <a name="filter-query"></a><span data-ttu-id="d4746-223">Filterquery</span><span class="sxs-lookup"><span data-stu-id="d4746-223">Filter query</span></span>

1. <span data-ttu-id="d4746-224">Configureer in het dialoogvenster **Query** de filtervoorwaarden voor verkoop- en projectfacturen of laat de voorwaarden leeg om alle ingediende facturen mee te nemen.</span><span class="sxs-lookup"><span data-stu-id="d4746-224">In the **Inquiry** dialog box, configure the filtering conditions for both sales invoices and project invoices, or leave the conditions blank to include all unsubmitted invoices.</span></span>

    ![Filtercriteria voor indienen instellen](media/e-Invoicing-services-get-started-ITA-Set-up-Submission-filter-criteria.png)

2. <span data-ttu-id="d4746-226">Selecteer **OK** om het dialoogvenster **Query** te sluiten.</span><span class="sxs-lookup"><span data-stu-id="d4746-226">Select **OK** to close the **Inquiry** dialog box.</span></span>
3. <span data-ttu-id="d4746-227">Klik op **OK** om de geselecteerde documenten in te dienen.</span><span class="sxs-lookup"><span data-stu-id="d4746-227">Select **OK** submit the selected documents.</span></span>

> <span data-ttu-id="d4746-228">![OPMERKING] Wanneer u voor het eerst een document via de service verzendt, wordt u gevraagd de verbinding met de invoegtoepassing voor elektronische facturering te bevestigen.</span><span class="sxs-lookup"><span data-stu-id="d4746-228">![NOTE] During your first attempt to submit a document through the service, you will be prompted to confirm the connection with the Electronic invoicing add-on.</span></span> <span data-ttu-id="d4746-229">Selecteer **Klik hier om verbinding te maken met de service voor het indienen van elektronische documenten**.</span><span class="sxs-lookup"><span data-stu-id="d4746-229">Select **Click here to connect to Electronic Document Submission Service**.</span></span>

#### <a name="view-submission-logs"></a><span data-ttu-id="d4746-230">Indieningslogboeken weergeven</span><span class="sxs-lookup"><span data-stu-id="d4746-230">View submission logs</span></span>

<span data-ttu-id="d4746-231">U kunt de indieningslogboeken voor alle ingediende documenten weergeven.</span><span class="sxs-lookup"><span data-stu-id="d4746-231">You can view the submission logs for all submitted documents.</span></span>

1. <span data-ttu-id="d4746-232">Ga naar **Organisatiebeheer \> Periodiek \> Elektronische documenten \> Indieningslogboek voor elektronische documenten**.</span><span class="sxs-lookup"><span data-stu-id="d4746-232">Go to **Organization administration \> Periodic \> Electronic documents \> Electronic document submission log**.</span></span>
2. <span data-ttu-id="d4746-233">Selecteer in het veld **Documenttype** de optie **Klantfactuurjournaal** of **Projectfactuur** om te filteren op de vereiste elektronische documenten.</span><span class="sxs-lookup"><span data-stu-id="d4746-233">In the **Document type** field, select **Customer invoice journal** or **Project invoice** to filter for the required electronic documents.</span></span>

    ![Een documenttype selecteren om de indieningslogboeken weer te geven](media/e-Invoicing-services-get-started-ITA-Select-Document-type-for-viewing-submission-log.png)

    <span data-ttu-id="d4746-235">De waarde die wordt weergegeven in de kolom **Indieningsstatus** staat voor de status van het indieningsproces.</span><span class="sxs-lookup"><span data-stu-id="d4746-235">The value that is shown in the **Submission status** column represents the status of the submission process.</span></span> <span data-ttu-id="d4746-236">Hiermee wordt aangegeven of het proces volgens de configuratie is uitgevoerd en of er aanvullende actie vereist is.</span><span class="sxs-lookup"><span data-stu-id="d4746-236">It indicates whether the process ran as configured and whether additional action is required.</span></span>

3. <span data-ttu-id="d4746-237">Selecteer in het actievenster **Query's \> Details van indiening** om de details van de uitvoeringslogboeken van indieningen weer te geven.</span><span class="sxs-lookup"><span data-stu-id="d4746-237">On the Action Pane, select **Inquiries \> Submission details** to view the details of the submission execution logs.</span></span>

    ![Details van indieningslogboeken weergeven](media/e-Invoicing-services-get-started-ITA-View-Submission-log-details.png)

4. <span data-ttu-id="d4746-239">Op het sneltabblad **Verwerkingsacties** kunt u het uitvoeringslogboek weergeven voor de acties die zijn geconfigureerd in de functieversie die is ingesteld in RCS.</span><span class="sxs-lookup"><span data-stu-id="d4746-239">On the **Processing actions** FastTab, you can view the execution log for the actions that are configured in the feature version that was set up in RCS.</span></span> <span data-ttu-id="d4746-240">De kolom **Status** geeft aan of de actie met goed gevolg is uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="d4746-240">The **Status** column shows whether the action was successfully run.</span></span>
5. <span data-ttu-id="d4746-241">Op het sneltabblad **Actiebestanden** kunt u de tussenliggende bestanden weergeven die zijn gegenereerd tijdens de uitvoering van de acties.</span><span class="sxs-lookup"><span data-stu-id="d4746-241">On the **Action files** FastTab, you can view the intermediate files that were generated during execution of the actions.</span></span> <span data-ttu-id="d4746-242">U kunt **Weergeven** selecteren om het uitvoer-XML-bestand in **FatturaPA**-indeling te downloaden en de inhoud weer te geven.</span><span class="sxs-lookup"><span data-stu-id="d4746-242">You can select **View** to download the output XML file in **FatturaPA** format and view its content.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d4746-243">Verwante onderwerpen</span><span class="sxs-lookup"><span data-stu-id="d4746-243">Related topics</span></span>

- [<span data-ttu-id="d4746-244">Overzicht van de invoegtoepassing voor elektronische facturering</span><span class="sxs-lookup"><span data-stu-id="d4746-244">Electronic invoicing add-on overview</span></span>](e-invoicing-service-overview.md)
- [<span data-ttu-id="d4746-245">Aan de slag met de invoegtoepassing voor elektronische facturering</span><span class="sxs-lookup"><span data-stu-id="d4746-245">Get started with the Electronic invoicing add-on</span></span>](e-invoicing-get-started.md)
- [<span data-ttu-id="d4746-246">De invoegtoepassing voor elektronische facturering instellen</span><span class="sxs-lookup"><span data-stu-id="d4746-246">Set up the Electronic invoicing add-on</span></span>](e-invoicing-setup.md)
