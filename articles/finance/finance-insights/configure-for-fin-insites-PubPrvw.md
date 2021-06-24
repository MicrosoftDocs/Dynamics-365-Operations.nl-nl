---
title: Configuratie voor Finance insights in openbare preview (preview) - versie 10.0.20 en hoger
description: In dit onderwerp wordt uitgelegd hoe u uw systeem configureert voor gebruik van de mogelijkheden die beschikbaar zijn in Finance Insights voor openbare preview in versie 10.0.20 en hoger.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-06-03
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 613bd4816e2f0c4fbb56cf79779a08c6a09592bd
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222607"
---
# <a name="configuration-for-finance-insights-for-public-preview-preview---version-10020-and-later"></a><span data-ttu-id="ccd5f-103">Configuratie voor Finance insights in openbare preview (preview) - versie 10.0.20 en hoger</span><span class="sxs-lookup"><span data-stu-id="ccd5f-103">Configuration for Finance insights for public preview (preview) - version 10.0.20 and later</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="ccd5f-104">Finance Insights combineert de functionaliteit van Microsoft Dynamics 365 Finance met Dataverse, Azure en AI Builder, zodat u beschikt over krachtige prognosefuncties voor uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-104">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="ccd5f-105">In dit onderwerp wordt uitgelegd hoe u Dynamics 365 Finance versie 10.0.20 configureert zodat uw systeem de mogelijkheden kan gebruiken die beschikbaar zijn in Finance Insights voor openbare preview.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-105">This topic explains how to configure Dynamics 365 Finance version 10.0.20 so that your system can use the capabilities that are available in Finance insights public preview.</span></span>

> [!NOTE]
> <span data-ttu-id="ccd5f-106">De configuratiestappen die in dit onderwerp worden beschreven, zijn alleen van toepassing op Finance versie 10.0.20 en hoger.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-106">The configuration steps that are described in this topic apply only to Finance version 10.0.20 and later.</span></span> <span data-ttu-id="ccd5f-107">Zie [Configuratie voor Finance Insights - versies tot en met 10.0.18](configure-for-fin-insites.md) als u Finance insights versie 10.0.19 en lager wilt instellen.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-107">'To set up Finance insights on version 10.0.19 and earlier, see [Configuration for Finance insights - versions up to 10.0.18](configure-for-fin-insites.md).</span></span>

## <a name="deploy-finance"></a><span data-ttu-id="ccd5f-108">Finance implementeren</span><span class="sxs-lookup"><span data-stu-id="ccd5f-108">Deploy Finance</span></span>

<span data-ttu-id="ccd5f-109">Ga als volgt te werk om de omgevingen te implementeren.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-109">Follow these steps to deploy the environments.</span></span>

1. <span data-ttu-id="ccd5f-110">In Microsoft Dynamics Lifecycle Services (LCS) kunt u een Finance-omgeving maken of bijwerken.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-110">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Finance environment.</span></span> <span data-ttu-id="ccd5f-111">Voor de omgeving is app-versie 10.0.20 of hoger van Finance and Operations-apps vereist.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-111">The environment requires app version 10.0.20 or later of Finance and Operations apps.</span></span>
2. <span data-ttu-id="ccd5f-112">De omgeving moet een omgeving met hoge beschikbaarheid (HA) zijn in de sandbox.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-112">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="ccd5f-113">(Dit type omgeving wordt ook wel een Tier-2-omgeving genoemd.) Zie [Omgevingsplanning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-113">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="ccd5f-114">Als u Finance insights configureert in een Sandbox-omgeving, moet u mogelijk productiegegevens naar die omgeving kopiëren om voorspellingen te kunnen uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-114">If you are configuring Finance insights in a Sandbox environment, you might need to copy production data to that environment for predictions to work.</span></span> <span data-ttu-id="ccd5f-115">Het voorspellingsmodel gebruikt meerdere jaren aan gegevens om voorspellingen samen te stellen.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-115">The prediction model uses multiple years of data to build predictions.</span></span> <span data-ttu-id="ccd5f-116">De Contoso-demonstratiegegevens bevatten niet voldoende historische gegevens om het voorspellingsmodel op een adequate manier te trainen.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-116">The Contoso demo data doesn’t contain enough historical data to train the prediction model adequately.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="ccd5f-117">Dataverse configureren</span><span class="sxs-lookup"><span data-stu-id="ccd5f-117">Configure Dataverse</span></span>

<span data-ttu-id="ccd5f-118">Voer de volgende stappen uit om Dataverse voor Finance Insights te configureren.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-118">Follow these steps to configure Dataverse for Finance insights.</span></span>

1. <span data-ttu-id="ccd5f-119">Open de omgevingspagina in LCS en controleer of de sectie **Power Platform-integratie** al is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-119">In LCS, open the environment page, and verify that the **Power Platform Integration** section is already set up.</span></span>

    - <span data-ttu-id="ccd5f-120">Als deze al is ingesteld, moet de naam van de Dataverse-omgeving worden weergegeven die is gekoppeld aan de Finance-omgeving.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-120">If it's already set up, the Dataverse environment name that is linked to the Finance environment should be listed.</span></span>
    - <span data-ttu-id="ccd5f-121">Als de sectie niet is ingesteld, voert u deze stappen uit:</span><span class="sxs-lookup"><span data-stu-id="ccd5f-121">If it isn't yet set up, follow these steps:</span></span>

        1. <span data-ttu-id="ccd5f-122">Selecteer **Instellingen** in de sectie **Power Platform**-integratie.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-122">In the **Power Platform Integration** section, select **Setup**.</span></span> <span data-ttu-id="ccd5f-123">De instelling van de omgeving kan maximaal een uur duren.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-123">Setup of the environment might take up to an hour.</span></span>
        2. <span data-ttu-id="ccd5f-124">Nadat de Dataverse-omgeving is ingesteld, moet de naam van de Dataverse-omgeving die is gekoppeld aan de Finance-omgeving worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-124">If the Dataverse environment is successfully set up, the Dataverse environment name that is linked to the Finance environment should be listed.</span></span>

        > [!NOTE]
        > <span data-ttu-id="ccd5f-125">Nadat u de omgevingsinstellingen hebt voltooid, moet u **Koppeling naar CDS for Apps** **niet** selecteren.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-125">After you complete the environment setup, do **not** select **Link to CDS for Apps**.</span></span> <span data-ttu-id="ccd5f-126">Deze knop is niet vereist voor Finance insights.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-126">This button isn't required for Finance insights.</span></span> <span data-ttu-id="ccd5f-127">Als u de knop selecteert, kunt u de vereiste omgevingsinvoegtoepassingen in LCS niet configureren.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-127">If you select it, you won't be able to configure the required environment add-ins in LCS.</span></span>

## <a name="configure-azure"></a><span data-ttu-id="ccd5f-128">Azure configureren</span><span class="sxs-lookup"><span data-stu-id="ccd5f-128">Configure Azure</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="ccd5f-129">De Azure Cloud Shell gebruiken om Data Lake-resources voor Finance Insights in te stellen</span><span class="sxs-lookup"><span data-stu-id="ccd5f-129">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="ccd5f-130">Windows PowerShell-script gebruiken</span><span class="sxs-lookup"><span data-stu-id="ccd5f-130">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="ccd5f-131">Er is een Windows PowerShell-script meegeleverd, zodat u eenvoudig de Azure-resources kunt instellen die worden beschreven in [Export naar Azure Data Lake configureren](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="ccd5f-131">A Windows PowerShell script has been provided so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span></span> <span data-ttu-id="ccd5f-132">Als u liever handmatig de instellingen opgeeft, slaat u deze procedure over en voltooit u de procedure in de sectie [Handmatige instellingen](#manual-setup) in plaats daarvan.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-132">If you prefer to do the setup manually, skip this procedure, and complete the procedure in the [Manual setup](#manual-setup) section instead.</span></span>

> [!NOTE]
> <span data-ttu-id="ccd5f-133">Voer de volgende procedure uit om het Windows PowerShell-script uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-133">Use the following procedure to run the Windows PowerShell script.</span></span> <span data-ttu-id="ccd5f-134">De instellingen werken mogelijk niet als u de optie **Probeer het** gebruikt in Azure CLI of als u het script op uw computer uitvoert.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-134">The setup might not work if you use the **Try it** option in Azure CLI or if you run the script on your computer.</span></span>

<span data-ttu-id="ccd5f-135">Voer de volgende stappen uit om Azure te configureren met het Windows PowerShell-script.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-135">Follow these steps to use the Windows PowerShell script to configure Azure.</span></span> <span data-ttu-id="ccd5f-136">U moet beschikken over rechten om een Azure-resourcegroep, Azure-resources en een Azure AD-toepassing te maken.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-136">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="ccd5f-137">Zie voor informatie over de vereiste machtigingen [Azure AD-machtigingen controleren](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span><span class="sxs-lookup"><span data-stu-id="ccd5f-137">For information about the required permissions, see [Check Azure AD permissions](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="ccd5f-138">Ga in de [Azure Portal](https://portal.azure.com) naar het Azure-abonnement van uw bestemming.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-138">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span>
2. <span data-ttu-id="ccd5f-139">Selecteer **Cloud Shell** rechts van het veld **Zoeken**.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-139">Select **Cloud Shell** to the right of the **Search** field.</span></span>
3. <span data-ttu-id="ccd5f-140">Selecteer **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-140">Select **PowerShell**.</span></span>
4. <span data-ttu-id="ccd5f-141">Maak opslagruimte als u dat wordt gevraagd.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-141">Create storage if you're prompted to create it.</span></span>
5. <span data-ttu-id="ccd5f-142">Selecteer op het tabblad **Azure CLI** de optie **Kopiëren**.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-142">On the **Azure CLI** tab, select **Copy**.</span></span>
6. <span data-ttu-id="ccd5f-143">Open een nieuw bestand in Kladblok en plak dit in het Windows PowerShell-script.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-143">In Notepad, open a new file, and paste in the Windows PowerShell script.</span></span>
7. <span data-ttu-id="ccd5f-144">Sla het bestand op met de naam **ConfigureDataLake.ps1**.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-144">Save the file as **ConfigureDataLake.ps1**.</span></span>
8. <span data-ttu-id="ccd5f-145">Upload het Windows PowerShell-script naar de sessie met de menuoptie voor uploaden in Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-145">Upload the Windows PowerShell script to the session by using the menu option for upload in Cloud Shell.</span></span>
9. <span data-ttu-id="ccd5f-146">Voer het script **.\ConfigureDataLake.ps1** uit.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-146">Run the **.\ConfigureDataLake.ps1** script.</span></span>
10. <span data-ttu-id="ccd5f-147">Volg de aanwijzingen om het script uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-147">Follow the prompts to run the script.</span></span>
11. <span data-ttu-id="ccd5f-148">Gebruik de informatie uit de scriptuitvoer om de invoegtoepassing Exporteren naar Data Lake in LCS te installeren.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-148">Use the information from the script output to install the Export to Data Lake add-in in LCS.</span></span>

### <a name="manual-setup"></a><span data-ttu-id="ccd5f-149">Handmatige installatie</span><span class="sxs-lookup"><span data-stu-id="ccd5f-149">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="ccd5f-150">Toepassingen toevoegen aan de Azure AD-tenant</span><span class="sxs-lookup"><span data-stu-id="ccd5f-150">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="ccd5f-151">Ga in de [Azure Portal](https://portal.azure.com) naar **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-151">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="ccd5f-152">Selecteer **Beheren \> Ondernemingstoepassingen**.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-152">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="ccd5f-153">Zoek naar de volgende toepassingen op app-id.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-153">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="ccd5f-154">Sollicitatie</span><span class="sxs-lookup"><span data-stu-id="ccd5f-154">Application</span></span>                              | <span data-ttu-id="ccd5f-155">App-id</span><span class="sxs-lookup"><span data-stu-id="ccd5f-155">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="ccd5f-156">Microsoft Dynamics ERP-microservices</span><span class="sxs-lookup"><span data-stu-id="ccd5f-156">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="ccd5f-157">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="ccd5f-157">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="ccd5f-158">Microsoft Dynamics ERP-microservices CDS</span><span class="sxs-lookup"><span data-stu-id="ccd5f-158">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="ccd5f-159">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="ccd5f-159">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="ccd5f-160">AI Builder-autorisatieservice</span><span class="sxs-lookup"><span data-stu-id="ccd5f-160">AI Builder Authorization Service</span></span>         | <span data-ttu-id="ccd5f-161">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="ccd5f-161">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="ccd5f-162">Als u geen van de voorgaande toepassingen kunt vinden, voert u de volgende stappen uit.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-162">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="ccd5f-163">Selecteer op uw lokale computer het menu **Start** en zoek naar **powershell**.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-163">On your local computer, on the **Start** menu, search for **powershell**.</span></span>
2. <span data-ttu-id="ccd5f-164">Selecteer **Windows PowerShell** en houd ingedrukt (of klik met de rechtermuisknop) en selecteer **Uitvoeren als beheerder**.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-164">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="ccd5f-165">Voer de volgende opdracht uit om de **AzureAD**-module te installeren.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-165">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="ccd5f-166">Als een NuGet-provider vereist is om door te gaan, selecteert u **J** om deze te installeren.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-166">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="ccd5f-167">Als u het bericht 'Niet-vertrouwde opslagplaats' ontvangt, selecteert u **J** om door te gaan.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-167">If you receive an "Untrusted repository" message, select **Y** to continue.</span></span>
6. <span data-ttu-id="ccd5f-168">Voer voor elke toepassing die moet worden toegevoegd de volgende opdrachten uit om de toepassing toe te voegen aan Azure AD.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-168">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="ccd5f-169">Meld u aan als Azure AD-beheerder als dat wordt gevraagd.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-169">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="ccd5f-170">Azure-resources maken</span><span class="sxs-lookup"><span data-stu-id="ccd5f-170">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="ccd5f-171">Zorg ervoor dat u de volgende resources in hetzelfde Azure AD-exemplaar maakt als waarin de Dataverse-omgeving zich bevindt.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-171">Make sure that you create the following resources in the same Azure AD instance that the Dataverse environment is in.</span></span> <span data-ttu-id="ccd5f-172">U kunt resources uit een ander Azure AD-exemplaar niet gebruiken.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-172">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="ccd5f-173">Een nieuw opslagaccount maken:</span><span class="sxs-lookup"><span data-stu-id="ccd5f-173">Create a storage account:</span></span>

    1. <span data-ttu-id="ccd5f-174">Maak een opslag account in de [Azure Portal](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="ccd5f-174">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="ccd5f-175">Stel in het dialoogvenster **Opslagaccount maken** de volgende velden in:</span><span class="sxs-lookup"><span data-stu-id="ccd5f-175">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="ccd5f-176">**Locatie**: selecteer het datacentrum waar uw omgeving zich bevindt.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-176">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="ccd5f-177">**Prestaties**: we raden u aan om **Standaard** te selecteren.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-177">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="ccd5f-178">**Soort account**: selecteer **StorageV2**.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-178">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="ccd5f-179">Selecteer **Inschakelen** onder **Hiërarchische naamruimten** in het dialoogvenster **Geavanceerde opties** voor de optie **Data Lake Storage Gen2**.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-179">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="ccd5f-180">Als u deze functie niet inschakelt, kunt u geen gegevens gebruiken die door Finance and Operations-apps worden geschreven met behulp van services zoals Power BI-gegevensstromen.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-180">If you don't enable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="ccd5f-181">Selecteer **Controleren en maken**.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-181">Select **Review and create**.</span></span> <span data-ttu-id="ccd5f-182">Wanneer de implementatie is voltooid, wordt de nieuwe resource weergegeven in de Azure Portal.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-182">When the deployment is completed, the new resource is shown in the Azure portal.</span></span>
    5. <span data-ttu-id="ccd5f-183">Ga naar het opslagaccount dat u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-183">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="ccd5f-184">Selecteer **Toegangssleutels** in het linkermenu.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-184">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="ccd5f-185">Kopieer de naam van het opslagaccount en sla deze op.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-185">Copy and save the name of the storage account.</span></span> <span data-ttu-id="ccd5f-186">Wanneer u de sleutelkluisgeheimen instelt, moet u deze waarde later opgeven.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-186">You will have to provide this value later, when you set up key vault secrets.</span></span>

2. <span data-ttu-id="ccd5f-187">Een sleutelkluis maken:</span><span class="sxs-lookup"><span data-stu-id="ccd5f-187">Create a key vault:</span></span>

    1. <span data-ttu-id="ccd5f-188">Maak een Key Vault in de [Azure Portal](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="ccd5f-188">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="ccd5f-189">Selecteer in het dialoogvenster **Key Vault maken** in het veld **Locatie** het datacentrum waar uw omgeving zich bevindt.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-189">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="ccd5f-190">Nadat de sleutelkluis is gemaakt, gaat u naar **Overzicht van Key Vault** en kopieert u de DNS-naam en slaat u deze op.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-190">After key vault is created, go to **Key Vault Overview**, and copy and save the DNS name.</span></span> <span data-ttu-id="ccd5f-191">Wanneer u de Data Lake-invoegtoepassing instelt, moet u deze waarde later opgeven.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-191">You will have to provide this value later, when you set up the Data Lake add-in.</span></span>

3. <span data-ttu-id="ccd5f-192">Een Azure AD-toepassing maken en registreren:</span><span class="sxs-lookup"><span data-stu-id="ccd5f-192">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="ccd5f-193">Ga in de [Azure Portal](https://portal.azure.com) naar **Azure Active Directory** en selecteer **App-registraties**.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-193">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="ccd5f-194">Selecteer **Nieuwe toepassingsregistratie** en stel de volgende velden in:</span><span class="sxs-lookup"><span data-stu-id="ccd5f-194">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="ccd5f-195">**Naam**: voer de naam van de app in.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-195">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="ccd5f-196">**Toepassingstype**: selecteer **Web-API**.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-196">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="ccd5f-197">**Omleidings-URL instellen**: voer de URL in voor uw Dynamics 365-exemplaar, bijvoorbeeld `https://yourdynamicsinstance.dynamics.com/auth`.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-197">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="ccd5f-198">Ga naar de app die u zojuist hebt gemaakt om de waarde van de **Toepassings-id (client)** te kopiëren en op te slaan.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-198">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="ccd5f-199">Wanneer u de sleutelkluisgeheimen instelt, moet u deze waarde later opgeven.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-199">You will have to provide this value later, when you set up key vault secrets.</span></span>
    4. <span data-ttu-id="ccd5f-200">Ga naar **API-machtigingen** en voer de volgende stappen uit:</span><span class="sxs-lookup"><span data-stu-id="ccd5f-200">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="ccd5f-201">Selecteer **Een machtiging toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-201">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="ccd5f-202">Selecteer **Azure Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-202">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="ccd5f-203">Nadat u gedelegeerde machtigingen hebt geselecteerd, selecteert u **gebruikers\_imitatie**.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-203">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="ccd5f-204">Selecteer **Machtigingen toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-204">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="ccd5f-205">Selecteer in het menu voor de app **Certificaten \& geheimen** en voer de volgende stappen uit om Key Vault-geheimen te maken:</span><span class="sxs-lookup"><span data-stu-id="ccd5f-205">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="ccd5f-206">Selecteer **Nieuw clientgeheim**.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-206">Select **New client secret**.</span></span>
        2. <span data-ttu-id="ccd5f-207">Voer in het veld **Sleutelbeschrijving** een naam in.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-207">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="ccd5f-208">Selecteer een duur en vervolgens **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-208">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="ccd5f-209">Er wordt een geheim gegenereerd in het veld **Waarde**.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-209">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="ccd5f-210">Kopieer de clientgeheimwaarde en sla deze op.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-210">Copy and save the client secret value.</span></span> <span data-ttu-id="ccd5f-211">Wanneer u de sleutelkluisgeheimen instelt, moet u deze waarde later opgeven.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-211">You will have to provide this value later, when you set up key vault secrets.</span></span>

4. <span data-ttu-id="ccd5f-212">Key Vault-geheimen maken:</span><span class="sxs-lookup"><span data-stu-id="ccd5f-212">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="ccd5f-213">Ga naar de Key Vault die u eerder hebt gemaakt en selecteer **Geheimen**.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-213">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="ccd5f-214">Voer de volgende stappen uit voor elke geheime naam in de onderstaande tabel:</span><span class="sxs-lookup"><span data-stu-id="ccd5f-214">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="ccd5f-215">Selecteer **Genereren/Importeren**.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-215">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="ccd5f-216">Selecteer in het dialoogvenster **Een geheim maken** in het veld **Opties voor uploaden** de optie **Handmatig**.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-216">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="ccd5f-217">Maak de geheime naam en waarde op basis van de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-217">Create the secret name and value from the table.</span></span>
        4. <span data-ttu-id="ccd5f-218">Selecteer **Ingeschakeld** en vervolgens **Maken**.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-218">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="ccd5f-219">Het geheim wordt gemaakt en toegevoegd aan Key Vault.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-219">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="ccd5f-220">Geheime naam</span><span class="sxs-lookup"><span data-stu-id="ccd5f-220">Secret name</span></span>                       | <span data-ttu-id="ccd5f-221">Geheime waarde</span><span class="sxs-lookup"><span data-stu-id="ccd5f-221">Secret value</span></span>                                                                                 |
        |-----------------------------------|----------------------------------------------------------------------------------------------|
        | <span data-ttu-id="ccd5f-222">app-id</span><span class="sxs-lookup"><span data-stu-id="ccd5f-222">app-id</span></span>                            | <span data-ttu-id="ccd5f-223">De app-id van de toepassing die u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-223">The app ID of the application that you created earlier.</span></span>                                      |
        | <span data-ttu-id="ccd5f-224">app-secret</span><span class="sxs-lookup"><span data-stu-id="ccd5f-224">app-secret</span></span>                        | <span data-ttu-id="ccd5f-225">Het clientgeheim dat u eerder hebt opgeslagen.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-225">The client secret that you saved earlier.</span></span>                                                    |
        | <span data-ttu-id="ccd5f-226">storage-account-name</span><span class="sxs-lookup"><span data-stu-id="ccd5f-226">storage-account-name</span></span>              | <span data-ttu-id="ccd5f-227">De naam van het opslagaccount dat u eerder hebt gemaakt, zoals **storageaccount1**.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-227">The name of the storage account that you created earlier, such as **storageaccount1**.</span></span>       |

5. <span data-ttu-id="ccd5f-228">De toepassing machtigen om toegang te krijgen tot de Key Vault:</span><span class="sxs-lookup"><span data-stu-id="ccd5f-228">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="ccd5f-229">Open in de [Azure Portal](https://portal.azure.com) de Key Vault die u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-229">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="ccd5f-230">Selecteer het toegangsbeleid.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-230">Select the access policies.</span></span>
    3. <span data-ttu-id="ccd5f-231">Voer de volgende stappen uit voor elke toepassing in de onderstaande tabel:</span><span class="sxs-lookup"><span data-stu-id="ccd5f-231">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="ccd5f-232">Selecteer **Toegangsbeleid toevoegen** om een toegangsbeleid te maken.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-232">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="ccd5f-233">Selecteer in het veld **Geheime machtigingen** de machtigingen uit de tabel.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-233">In the **Secret permissions** field, select the permissions from the table.</span></span>
        3. <span data-ttu-id="ccd5f-234">Zoek in het veld **Principal selecteren** de weergavenaam van de toepassing uit de tabel.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-234">In the **Select principal** field, search for the application display name from the table.</span></span>
        4. <span data-ttu-id="ccd5f-235">Selecteer **Selecteren**.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-235">Select **Select**.</span></span>
        5. <span data-ttu-id="ccd5f-236">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-236">Select **Add**.</span></span>
        6. <span data-ttu-id="ccd5f-237">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-237">Select **Save**.</span></span>

        | <span data-ttu-id="ccd5f-238">Sollicitatie</span><span class="sxs-lookup"><span data-stu-id="ccd5f-238">Application</span></span>                                              | <span data-ttu-id="ccd5f-239">Machtigingen</span><span class="sxs-lookup"><span data-stu-id="ccd5f-239">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="ccd5f-240">De weergavenaam van de nieuwe toepassing die u hebt gemaakt</span><span class="sxs-lookup"><span data-stu-id="ccd5f-240">The display name of the new application that you created</span></span> | <span data-ttu-id="ccd5f-241">Ophalen, Lijst</span><span class="sxs-lookup"><span data-stu-id="ccd5f-241">Get, List</span></span>   |
        | <span data-ttu-id="ccd5f-242">**Microsoft Dynamics ERP-microservices**</span><span class="sxs-lookup"><span data-stu-id="ccd5f-242">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="ccd5f-243">Ophalen, Lijst</span><span class="sxs-lookup"><span data-stu-id="ccd5f-243">Get, List</span></span>   |

6. <span data-ttu-id="ccd5f-244">Rollen toewijzen voor toegang tot het opslagaccount:</span><span class="sxs-lookup"><span data-stu-id="ccd5f-244">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="ccd5f-245">Open in de [Azure Portal](https://portal.azure.com) het opslagaccount dat u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-245">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="ccd5f-246">Selecteer **Access Control (IAM)** en vervolgens **Roltoewijzingen**.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-246">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="ccd5f-247">Selecteer **Toevoegen, Roltoewijzing toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-247">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="ccd5f-248">Voer de volgende stappen uit voor elke toepassing in de onderstaande tabel:</span><span class="sxs-lookup"><span data-stu-id="ccd5f-248">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="ccd5f-249">Selecteer de rol in de tabel.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-249">Select the role from the table.</span></span>
        2. <span data-ttu-id="ccd5f-250">Laat het veld **Toegang toewijzen aan** ingesteld staan op **Azure AD-gebruiker, -groep of serviceprincipal**.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-250">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="ccd5f-251">Voer in het veld **Selecteren** de toepassing uit de tabel in.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-251">In the **Select** field, enter the application from the table.</span></span>
        4. <span data-ttu-id="ccd5f-252">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-252">Select **Save**.</span></span>

        | <span data-ttu-id="ccd5f-253">Sollicitatie</span><span class="sxs-lookup"><span data-stu-id="ccd5f-253">Application</span></span>                                              | <span data-ttu-id="ccd5f-254">Rol</span><span class="sxs-lookup"><span data-stu-id="ccd5f-254">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="ccd5f-255">De weergavenaam van de nieuwe toepassing die u hebt gemaakt</span><span class="sxs-lookup"><span data-stu-id="ccd5f-255">The display name of the new application that you created</span></span> | <span data-ttu-id="ccd5f-256">Eigenaar</span><span class="sxs-lookup"><span data-stu-id="ccd5f-256">Owner</span></span>                       |
        | <span data-ttu-id="ccd5f-257">De weergavenaam van de nieuwe toepassing die u hebt gemaakt</span><span class="sxs-lookup"><span data-stu-id="ccd5f-257">The display name of the new application that you created</span></span> | <span data-ttu-id="ccd5f-258">Inzender</span><span class="sxs-lookup"><span data-stu-id="ccd5f-258">Contributor</span></span>                 |
        | <span data-ttu-id="ccd5f-259">De weergavenaam van de nieuwe toepassing die u hebt gemaakt</span><span class="sxs-lookup"><span data-stu-id="ccd5f-259">The display name of the new application that you created</span></span> | <span data-ttu-id="ccd5f-260">Inzender voor opslagaccounts</span><span class="sxs-lookup"><span data-stu-id="ccd5f-260">Storage Account Contributor</span></span> |
        | <span data-ttu-id="ccd5f-261">De weergavenaam van de nieuwe toepassing die u hebt gemaakt</span><span class="sxs-lookup"><span data-stu-id="ccd5f-261">The display name of the new application that you created</span></span> | <span data-ttu-id="ccd5f-262">Eigenaar van gegevens in opslagblob</span><span class="sxs-lookup"><span data-stu-id="ccd5f-262">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="ccd5f-263">**AI Builder-autorisatieservice**</span><span class="sxs-lookup"><span data-stu-id="ccd5f-263">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="ccd5f-264">Lezer van gegevens in opslagblob</span><span class="sxs-lookup"><span data-stu-id="ccd5f-264">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="ccd5f-265">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="ccd5f-265">Azure CLI</span></span>](#tab/azure-azure-cli)

```
function New-FinanceDataLakeAzureResources {
    Assert-ScriptSetup

    $ClientAppName = 'Finance Data Lake Application'
    $DefaultSecretExpiryInYear = 1
    $MicrosoftDynamicsERPMicroservicesAppId = '0cdb527f-a8d1-4bf8-9436-b352c68682b2'
    $MicrosoftDynamicsERPMicroservicesCDSAppId = '703e2651-d3fc-48f5-942c-74274233dba8'
    $AIBuilderAuthorizationServiceAppId = 'ad40333e-9910-4b61-b281-e3aeeb8c3ef3'
    $KeyVaultServicePrincipalAppId = 'cfa8b339-82a2-471a-a3c9-0fc0be7a4093'
    $GraphServicePrincipalAppId = '00000003-0000-0000-c000-000000000000'

    Import-Module AzureAD.Standard.Preview
    $connectAzureADParameters = @{ 'Identity' = $true; 'TenantId' = $env:ACC_TID }
    $azContext = AzureAD.Standard.Preview\Connect-AzureAD @connectAzureADParameters
    $userContext = ConvertFrom-Json ((az ad signed-in-user show) -join '')
    $user = Get-AzureADUser -Filter ("UserPrincipalName eq '" + $userContext.UserPrincipalName + "'")

    Set-AzureSubscription
    
    $resourceGroup = $null
    $ResourceGroupName = 'D365FinanceInsightsDataLake'
    $ResourceGroupNameSuffix = ''
    $FullResourceGroupName = ''
    Write-Output ("The default Azure Resource Group name is '{0}'" -f $ResourceGroupName)
    while (-not ($resourceGroup)) {
        $ResourceGroupNameSuffix = (Read-Host -Prompt "Enter optional Azure Resource Group name suffix: (leave blank for no suffix)")
        if ([string]::IsNullOrWhitespace($ResourceGroupNameSuffix))
        {
            $FullResourceGroupName = $ResourceGroupName
        }
        else
        {
            if ($ResourceGroupNameSuffix -notmatch "^[A-Za-z0-9]+$") {
                Write-Warning "The Azure Resource Group name suffix can only include alphanumeric characters."
                continue
            }

            if ($ResourceGroupNameSuffix.Length -gt 60) {
                Write-Warning "The Azure Resource Group name suffix cannot be longer than 60 characters."
                continue
            }

            $FullResourceGroupName = $ResourceGroupName + $ResourceGroupNameSuffix
        }
        
        $resourceGroup = Get-AzResourceGroup -Name $FullResourceGroupName -ErrorAction SilentlyContinue

        if (-not ($resourceGroup)) {
            Write-Output ("Your new Azure Resource Group name is '{0}'" -f $FullResourceGroupName)
            $resourceLocation = ''
            $azResourceLocations = (Get-AzLocation | Select-Object Location).Location
            while ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations))) {
                $resourceLocation = (Read-Host -Prompt "Enter the location in which to create the Azure Resource Group: ('help' to see values)")
                if ($resourceLocation -eq 'help') {
                    Write-Output ("List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
                elseif ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations)))
                {
                    Write-Warning ("The provided location is not available for resource group. List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
            }
            $resourceGroup = New-AzResourceGroup -Name $FullResourceGroupName -Location $resourceLocation
            Write-Output ("Created Azure Resource Group '{0}'" -f $resourceGroup.ResourceGroupName)
        }
        else {
            Write-Output ("Found Azure Resource Group '{0}'" -f ($resourceGroup.ResourceGroupName))
        }
    }

    Write-Output '================================================================================='
    $MicrosoftDynamicsERPMicroservicesAppObjectId = Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesAppId
    Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesCDSAppId | Out-Null
    $aibuilderAuthorizationServiceObjectId = Create-ADServicePrincipal -AppId $AIBuilderAuthorizationServiceAppId
    Write-Output ('=================================================================================')

    $clientAppSPN = Get-AzureADServicePrincipal -Filter ("DisplayName eq '" + $ClientAppName + "'")
    if (-not ($clientAppSPN)) {
        $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        if (-not $keyVaultPrincipal)
        {
            New-AzureADServicePrincipal -AppId $KeyVaultServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Key Vault principal to AAD"
            $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        }
        $keyVaultAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $keyVaultAccess.ResourceAppId = $keyVaultPrincipal.AppId
        $keyVaultAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $keyVaultPrincipal.Oauth2Permissions.Id, "Scope")

        $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        if (-not $graphPrincipal)
        {
            New-AzureADServicePrincipal -AppId $GraphServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Graph principal to AAD"
            $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        }
        $userRead = $graphPrincipal.Oauth2Permissions | Where-Object { $_.Type -eq "User" -and $_.Value -eq "User.Read" }
        $graphAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $graphAccess.ResourceAppId = $graphPrincipal.AppId
        $graphAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $userRead.Id, "Scope")

        $clientApp = New-AzureADApplication -DisplayName $ClientAppName -RequiredResourceAccess @($keyVaultAccess, $graphAccess)
        $clientAppSPN = New-AzureADServicePrincipal -AppId $clientApp.AppId -Tags @($ClientAppName)
        $clientAppId = $clientApp.AppId
        Write-Output ('Created App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
    else {
        $clientApp = Get-AzureADApplication -Filter ("DisplayName eq '" + $ClientAppName + "'")
        $clientAppId = $clientApp.AppId
        Write-Output ('Found App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
            
    $clientAppSecretCredential = New-AzureADApplicationPasswordCredential -ObjectId $clientApp.ObjectId -CustomKeyIdentifier "ClientAppAccessKey" -EndDate (get-date).AddYears($DefaultSecretExpiryInYear)
    $ClientAppSecret = $clientAppSecretCredential.Value
    $clientAppSpId = $clientAppSPN.ObjectId

    Write-Output ('Generated application secret: ' + $ClientAppSecret)
    Write-Output '================================================================================='

    $templateObject = ConvertFrom-Json $azureTemplate -AsHashtable
    $templateObject.{$schema} = "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#"
    Write-Output 'Provisioning Azure resources. This may take a few minutes.'
    try {
        $deployment = New-AzResourceGroupDeployment -ResourceGroupName $FullResourceGroupName -TemplateObject $templateObject -aibuilderAppObjectId $aibuilderAuthorizationServiceObjectId -clientAppId $clientAppId -clientAppSecret $ClientAppSecret -clientAppSpObjectId  $clientAppSpId -microserviceSpObjectId $MicrosoftDynamicsERPMicroservicesAppObjectId -userSpObjectId $user.ObjectId -Force -ErrorAction Stop
    }
    catch {
        $ErrorMessage = $_.Exception.Message
        if ($ErrorMessage.Contains("not allowed to be updated"))
        {
            Write-Error ($ErrorMessage)
            Write-Warning "Some items in the existing resource group $FullResourceGroupName could not be updated. To resolve the issue, remove the existing resource group $FullResourceGroupName and run the script again."
        }
        else {
            throw
        }

    }
    if ($deployment.ProvisioningState -eq 'Succeeded') {
        Write-Output "Successfully deployed the following resources to Azure:"
        Write-Output ("  Key Vault:                         " + $deployment.Outputs.keyVaultName.Value)
        Write-Output ("  Storage Account:                   " + $deployment.Outputs.storageAccountName.Value)
        
        $keyVault = Get-AzKeyVault -VaultName $deployment.Outputs.keyVaultName.Value
        $tenantId = (Get-AzContext).Tenant.Id

        Write-Output "Values for LCS Data Lake Add-In:"
        Write-Output ("  Tenant ID:                         " + $tenantId)
        Write-Output ("  DNS Name:                          " + $keyVault.VaultUri)
        Write-Output "  Storage account secret name:       storage-account-name"
        Write-Output "  Application ID secret name:        app-id"
        Write-Output "  Application Secret secret name:    app-secret"
        Write-Warning "Copy this information for the LCS Add-in for easy access. Azure Cloud Shell will eventually time out and close."

        Write-Output '================================================================================='
        Write-Output "Values for System parameters > Data connections:"
        Write-Output ("  Application ID:                    " + $clientAppId)
        Write-Output ("  Application Secret:                " + $ClientAppSecret)
        Write-Output ("  DNS name:                          " + $keyVault.VaultUri)
        Write-Output "  Secret name:                       storage-account-connection-string"
        Write-Warning "Copy this information for the System parameters for easy access. Azure Cloud Shell will eventually time out and close."
    }
    else {
        Write-Output ("Provisioning Azure resources failed with the following state: " + $deployment.ProvisioningState)
        Write-Output ("Some of the resources may have been created in resource group: " + $FullResourceGroupName)
    }
}

function Assert-ScriptSetup {
    if ($PSVersionTable.PSEdition -ne 'Core' -or -not $env:ACC_TID) { 
        throw "This script needs to be uploaded and run from Azure Cloud Shell (PowerShell)." 
    }
    
    if ((Get-AzContext) -eq $null -and (Connect-AzAccount) -eq $null) {
        throw 'Unable to connect to Azure account.'
    }
}

function Set-AzureSubscription {
    $azSubscription = $null
    while (-not ($azSubscription)) {
        $subscriptionId = (Read-Host -Prompt "Enter the Azure Subscription ID: (leave blank for default)")
        if ([string]::IsNullOrWhitespace($subscriptionId)){
            break
        }
        elseif (-not [guid]::TryParse($subscriptionId, $([ref][guid]::Empty))) {
                Write-Warning "Azure Subscription ID must be a valid GUID."
                continue
        }

        $azSubscription = Select-AzSubscription -SubscriptionId $subscriptionId
    }
}

function Create-ADServicePrincipal {
    param (
        [string] $AppId
    )

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $AppId | Out-Null
        $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
        Write-Host ("Added AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }
    else {
        Write-Host ("Found AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }

    return $service.ObjectId
}

$azureTemplate = @"
{
    "contentVersion": "1.0.0.0",
    "parameters": {
      "aibuilderAppObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of the AI Builder application."
        }
      },
      "clientAppId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the application ID of client application."
        }
      },
      "clientAppSecret": {
        "type": "String",
        "metadata": {
          "description": "Specifies the Azure App ID client secret to in azure key vault."
        }
      },
      "clientAppSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of a client application service principal."
        }
      },
      "userSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of tenant admin service principal."
        }
      },
      "microserviceSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of Microsoft Dynamics ERP Microservices service principal."
        }
      },
      "storageAccountType": {
        "type": "string",
        "defaultValue": "Standard_LRS",
        "allowedValues": [
          "Standard_LRS",
          "Standard_GRS",
          "Standard_ZRS",
          "Premium_LRS"
        ],
        "metadata": {
          "description": "Storage Account type"
        }
      }
    },
    "variables": {
      "storageAccountApiVersion": "2019-06-01",
      "keyVaultApiVersion": "2018-02-14",
      "secretsPermissions": [
        "list",
        "get"
      ],
      "location": "[resourceGroup().location]",
      "storageAccountName": "[concat('store', uniquestring(resourceGroup().id))]",
      "keyVaultName": "[concat('keyvault', uniquestring(resourceGroup().id))]",
      "owner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '8e3af657-a8ff-443c-a75c-2fe8c4bcb635')]",
      "contributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b24988ac-6180-42a0-ab88-20f7382dd24c')]",
      "storageAccountContributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '17d1049b-9a84-46fb-8f53-869881c3d3ab')]",
      "storageBlobDataOwner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b7e6dc6d-f1e8-4753-8033-0f276bb0955b')]",
      "storageBlobDataReader": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '2a2b9908-6ea1-4ae2-8e65-a410df84e7d1')]"
    },
    "resources": [
      {
        "type": "Microsoft.Storage/storageAccounts",
        "apiVersion": "[variables('storageAccountApiVersion')]",
        "name": "[variables('storageAccountName')]",
        "location": "[variables('location')]",
        "sku": {
          "name": "[parameters('storageAccountType')]"
        },
        "kind": "StorageV2",
        "properties": {
          "accessTier": "Hot",
          "supportsHttpsTrafficOnly": true,
          "isHnsEnabled": true
        },
        "resources": [
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'1')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('owner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'2')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('contributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'3')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageAccountContributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'4')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataOwner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'5')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataReader')]",
              "principalId": "[parameters('aibuilderAppObjectId')]"
            }
          }
        ]
      },
      {
        "type": "Microsoft.KeyVault/vaults",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "name": "[variables('keyVaultName')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName'))]"
        ],
        "tags": {
        },
        "properties": {
          "enabledForDeployment": false,
          "enabledForTemplateDeployment": false,
          "enabledForDiskEncryption": false,
          "enableRbacAuthorization": false,
          "accessPolicies": [
            {
              "objectId": "[parameters('clientAppSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('microserviceSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('userSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            }
          ],
          "tenantId": "[subscription().tenantId]",
          "sku": {
            "name": "Standard",
            "family": "A"
          },
          "enableSoftDelete": false,
          "networkAcls": {
            "defaultAction": "Allow",
            "bypass": "AzureServices"
          }
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-id')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppId')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-secret')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppSecret')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-name')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[variables('storageAccountName')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-connection-string')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[concat('DefaultEndpointsProtocol=https;AccountName=', variables('storageAccountName'), ';AccountKey=', listKeys(resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName')), variables('storageAccountApiVersion')).keys[0].value, ';EndpointSuffix=core.windows.net')]"
        }
      }
    ],
    "outputs": {
      "storageAccountName": {
        "type": "string",
        "value": "[variables('storageAccountName')]"
      },
      "keyVaultName": {
        "type": "string",
        "value": "[variables('keyVaultName')]"
      }
    }
  }
"@

try {
  Start-Transcript -path (Join-Path $HOME Provision-FinInsights-Azure.log)
  New-FinanceDataLakeAzureResources
}
catch {
  Write-Error $_.Exception.Message

  if ($PSItem.Exception.StackTrace -ne $null)
  {
      Write-Warning $_.Exception.StackTrace
  }

  $inner = $_.Exception.InnerException
  while ($null -ne $inner) {
    Write-Output 'Inner Exception:'
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $inner.InnerException
  }
}
finally {
  Stop-Transcript
}
```
---

## <a name="configure-the-export-to-data-lake-add-in"></a><span data-ttu-id="ccd5f-266">Invoegtoepassing Export naar Data Lake configureren</span><span class="sxs-lookup"><span data-stu-id="ccd5f-266">Configure the Export to Data Lake add-in</span></span>

<span data-ttu-id="ccd5f-267">Voer de volgende stappen uit om de invoegtoepassing Export naar Data Lake aan de omgeving toe te voegen met LCS.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-267">Follow these steps to use LCS to add the Export to Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="ccd5f-268">Meld u aan bij LCS en selecteer vervolgens **Volledige details** onder de naam van de omgeving aan de rechterkant van de pagina.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-268">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="ccd5f-269">Selecteer in de sectie **Invoegtoepassingen voor omgeving** de optie **Een nieuwe invoegtoepassing installeren**.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-269">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="ccd5f-270">Selecteer de invoegtoepassing **Exporteren naar Data Lake**.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-270">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="ccd5f-271">Voer de volgende waarden in.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-271">Enter the following values.</span></span>

    | <span data-ttu-id="ccd5f-272">Waarde</span><span class="sxs-lookup"><span data-stu-id="ccd5f-272">Value</span></span>                                                              | <span data-ttu-id="ccd5f-273">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="ccd5f-273">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="ccd5f-274">De tenant-id van het Azure-abonnement waarin de Key Vault zich bevindt</span><span class="sxs-lookup"><span data-stu-id="ccd5f-274">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="ccd5f-275">De tenant-id waar het opslagaccount, de apps en de key vaults zich bevinden.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-275">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="ccd5f-276">Als u deze waarde wilt verkrijgen, opent u de [Azure Portal](https://portal.azure.com), gaat u naar **Azure Active Directory** en kopieert u de waarde van **Tenant-id**.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-276">To obtain this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="ccd5f-277">Geef de DNS-naam op van uw Key Vault</span><span class="sxs-lookup"><span data-stu-id="ccd5f-277">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="ccd5f-278">De DNS-naam van de Key Vault, zoals `https://customkeyvault.vault.azure.net/`.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-278">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> |
    | <span data-ttu-id="ccd5f-279">Het geheim opgeven dat de naam van het opslagaccount bevat</span><span class="sxs-lookup"><span data-stu-id="ccd5f-279">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="ccd5f-280">**storage-account-name**</span><span class="sxs-lookup"><span data-stu-id="ccd5f-280">**storage-account-name**</span></span> |
    | <span data-ttu-id="ccd5f-281">Geheime naam voor de app-ID die moet worden gebruikt voor toegang tot Data Lake</span><span class="sxs-lookup"><span data-stu-id="ccd5f-281">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="ccd5f-282">**app-id**</span><span class="sxs-lookup"><span data-stu-id="ccd5f-282">**app-id**</span></span> |
    | <span data-ttu-id="ccd5f-283">Geheime naam voor clientgeheim van app</span><span class="sxs-lookup"><span data-stu-id="ccd5f-283">Secret name for App client secret</span></span>                                  | <span data-ttu-id="ccd5f-284">**app-secret**</span><span class="sxs-lookup"><span data-stu-id="ccd5f-284">**app-secret**</span></span> |

5. <span data-ttu-id="ccd5f-285">Ga akkoord met de voorwaarden en selecteer vervolgens **Installeren**.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-285">Agree to the terms, and then select **Install**.</span></span>

<span data-ttu-id="ccd5f-286">De invoegtoepassing wordt binnen enkele minuten geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-286">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-the-finance-insights-add-in"></a><span data-ttu-id="ccd5f-287">De invoegtoepassing Finance insights configureren</span><span class="sxs-lookup"><span data-stu-id="ccd5f-287">Configure the Finance insights add-in</span></span>

> [!NOTE]
> <span data-ttu-id="ccd5f-288">Als u de invoegtoepassing Inzichten ophalen eerder hebt geïnstalleerd, moet u de installatie ongedaan maken voordat u de volgende procedure voltooit.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-288">If you previously installed the Get insights add-in, uninstall it before you complete the following procedure.</span></span>

<span data-ttu-id="ccd5f-289">Voer de volgende stappen uit om de invoegtoepassing Finance insights te installeren.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-289">Follow these steps to install the Finance insights add-in.</span></span>

1. <span data-ttu-id="ccd5f-290">Meld u aan bij LCS en selecteer vervolgens **Volledige details** onder de naam van de omgeving aan de rechterkant van de pagina.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-290">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="ccd5f-291">Selecteer in de sectie **Invoegtoepassingen voor omgeving** de optie **Een nieuwe invoegtoepassing installeren**.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-291">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="ccd5f-292">Selecteer de invoegtoepassing **Finance insights**.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-292">Select the **Finance insights** add-in.</span></span>
4. <span data-ttu-id="ccd5f-293">Ga akkoord met de voorwaarden en selecteer vervolgens **Installeren**.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-293">Agree to the terms, and then select **Install**.</span></span>

## <a name="feedback-and-support"></a><span data-ttu-id="ccd5f-294">Feedback en ondersteuning</span><span class="sxs-lookup"><span data-stu-id="ccd5f-294">Feedback and support</span></span>

<span data-ttu-id="ccd5f-295">Stuur een e-mail naar [Finance insights (preview)](mailto:fiap@microsoft.com) als u feedback wilt geven of ondersteuning nodig hebt.</span><span class="sxs-lookup"><span data-stu-id="ccd5f-295">If you're interested in providing feedback, or if you require support, send an email to [Finance insights (Preview)](mailto:fiap@microsoft.com).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
