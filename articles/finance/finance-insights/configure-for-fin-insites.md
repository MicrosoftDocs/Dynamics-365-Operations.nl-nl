---
title: Configuratie voor Finance Insights - versies tot en met 10.0.19
description: In dit onderwerp worden de configuratiestappen beschreven die ervoor zorgen dat uw systeem de mogelijkheden gebruikt die beschikbaar zijn in Finance Insights voor versies tot en met 10.0.19.
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
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 6ad06bb6d041fc060b3a99538f6d4d0af333180f
ms.sourcegitcommit: ebcd9019cbb88a7f2afd9e701812e222566fd43d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/04/2021
ms.locfileid: "6186415"
---
# <a name="configuration-for-finance-insights-preview"></a><span data-ttu-id="31f74-103">Configuratie voor Finance Insights (preview)</span><span class="sxs-lookup"><span data-stu-id="31f74-103">Configuration for Finance insights (preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="31f74-104">De volgende procedures voor het instellen van Finance insights zijn geldig voor Microsoft Dynamics 365 Finance, versies tot en met 10.0.19.</span><span class="sxs-lookup"><span data-stu-id="31f74-104">The following procedures for setting up Finance insights are valid for Microsoft Dynamics 365 Finance versions up to 10.0.19.</span></span> <span data-ttu-id="31f74-105">Zie [Configuratie voor Finance Insights (preview) - versies 10.0.20 en hoger](configure-for-fin-insites-PubPrvw.md) als u Finance insights versie 10.0.20 en hoger wilt instellen.</span><span class="sxs-lookup"><span data-stu-id="31f74-105">To set up Finance insights on version 10.0.20 and later, see [Configuration for Finance Insights (preview) - versions 10.0.20 and beyond](configure-for-fin-insites-PubPrvw.md).</span></span>

<span data-ttu-id="31f74-106">Finance Insights combineert de functionaliteit van Microsoft Dynamics 365 Finance met Microsoft Dataverse, Azure en AI Builder, zodat u beschikt over krachtige prognosefuncties voor uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="31f74-106">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Microsoft Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="31f74-107">In dit onderwerp worden de configuratiestappen beschreven die ervoor zorgen dat uw systeem de mogelijkheden gebruikt die beschikbaar zijn in Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="31f74-107">This topic explains the configuration steps that will enable your system to use the capabilities that are available in Finance insights.</span></span>

## <a name="deploy-dynamics-365-finance"></a><span data-ttu-id="31f74-108">Dynamics 365 Finance implementeren</span><span class="sxs-lookup"><span data-stu-id="31f74-108">Deploy Dynamics 365 Finance</span></span>

<span data-ttu-id="31f74-109">Ga als volgt te werk om de omgevingen te implementeren.</span><span class="sxs-lookup"><span data-stu-id="31f74-109">Deploy the environments by following these steps.</span></span>

1. <span data-ttu-id="31f74-110">In Microsoft Dynamics Lifecycle Services (LCS) kunt u een Dynamics 365 Finance-omgeving maken of bijwerken.</span><span class="sxs-lookup"><span data-stu-id="31f74-110">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Dynamics 365 Finance environment.</span></span> <span data-ttu-id="31f74-111">Voor de omgeving is app-versie 10.0.11/Platform update 35 of hoger vereist.</span><span class="sxs-lookup"><span data-stu-id="31f74-111">The environment requires app version 10.0.11/Platform update 35 or later.</span></span>
2. <span data-ttu-id="31f74-112">De omgeving moet een omgeving met hoge beschikbaarheid (HA) zijn in de sandbox.</span><span class="sxs-lookup"><span data-stu-id="31f74-112">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="31f74-113">(Dit type omgeving wordt ook wel een Tier-2-omgeving genoemd.) Zie [Omgevingsplanning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="31f74-113">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="31f74-114">Als u Finance insights configureert in een Sandbox-omgeving, moet u mogelijk productiegegevens naar die omgeving kopiëren om voorspellingen te kunnen uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="31f74-114">If you are configuring Finance insights in a Sandbox environment, you might need to copy production data to that environment for predictions to work.</span></span> <span data-ttu-id="31f74-115">Het voorspellingsmodel gebruikt meerdere jaren aan gegevens om voorspellingen samen te stellen.</span><span class="sxs-lookup"><span data-stu-id="31f74-115">The prediction model uses multiple years of data to build predictions.</span></span> <span data-ttu-id="31f74-116">De Contoso-demonstratiegegevens bevatten niet voldoende historische gegevens om het voorspellingsmodel op een adequate manier te trainen.</span><span class="sxs-lookup"><span data-stu-id="31f74-116">The Contoso demo data doesn’t contain enough historical data to train the prediction model adequately.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="31f74-117">Dataverse configureren</span><span class="sxs-lookup"><span data-stu-id="31f74-117">Configure Dataverse</span></span>

<span data-ttu-id="31f74-118">Met de volgende stappen kunt u Dataverse configureren voor Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="31f74-118">Use the following steps to configure Dataverse for Finance insights.</span></span>

1. <span data-ttu-id="31f74-119">Open de omgevingspagina in LCS en controleer of de sectie **Power Platform-integratie** al is ingesteld.</span><span class="sxs-lookup"><span data-stu-id="31f74-119">Open the environment page in LCS and verify that the **Power Platform Integration** section is already setup.</span></span>
    1. <span data-ttu-id="31f74-120">Als deze al is ingesteld, moet de naam worden vermeld van de Dataverse-omgeving die is gekoppeld aan de Dynamics 365 Finance-omgeving.</span><span class="sxs-lookup"><span data-stu-id="31f74-120">If it is already set up, the Dataverse environment name linked to the Dynamics 365 Finance Environment should be listed.</span></span> <span data-ttu-id="31f74-121">Kopieer de naam van de Dataverse-omgeving.</span><span class="sxs-lookup"><span data-stu-id="31f74-121">Copy the Dataverse environment name.</span></span>
    2. <span data-ttu-id="31f74-122">Als de sectie niet is ingesteld, volgt u deze stappen:</span><span class="sxs-lookup"><span data-stu-id="31f74-122">If it is not set up, follow these steps:</span></span>
        1. <span data-ttu-id="31f74-123">Selecteer de knop **Instellingen** in de sectie Power Platform-integratie.</span><span class="sxs-lookup"><span data-stu-id="31f74-123">Select the **Setup** button in the Power Platform Integration section.</span></span> <span data-ttu-id="31f74-124">Het instellen van de omgeving kan tot een uur duren.</span><span class="sxs-lookup"><span data-stu-id="31f74-124">It may take up to an hour for the environment to be set up.</span></span>
        2. <span data-ttu-id="31f74-125">Nadat de Dataverse-omgeving is ingesteld, moet de naam van de Dataverse-omgeving die is gekoppeld aan de Dynamics 365 Finance-omgeving in de lijst zijn vermeld.</span><span class="sxs-lookup"><span data-stu-id="31f74-125">If the Dataverse environment is successfully set up, the Dataverse environment name linked to the Dynamics 365 Finance Environment should be listed.</span></span> <span data-ttu-id="31f74-126">Kopieer de naam van de Dataverse-omgeving.</span><span class="sxs-lookup"><span data-stu-id="31f74-126">Copy the Dataverse environment name.</span></span>
> [!NOTE]
> <span data-ttu-id="31f74-127">Let erop dat u, nadat de omgeving is ingesteld, de knop **Koppelen aan CDS for Apps** **NIET** selecteert.</span><span class="sxs-lookup"><span data-stu-id="31f74-127">After completing the environment set up, **DO NOT** select the **Link to CDS for Apps** button.</span></span> <span data-ttu-id="31f74-128">Dit is niet nodig voor Finance Insights en schakelt de mogelijkheid uit om de vereiste omgevings-invoegtoepassingen in LCS te voltooien.</span><span class="sxs-lookup"><span data-stu-id="31f74-128">This is not needed for Finance Insights and will disable the ability to complete the required Environment Add-ins in LCS.</span></span>

2. <span data-ttu-id="31f74-129">Open het [Power Platform-beheercentrum](https://admin.powerplatform.microsoft.com/) en voer de volgende stappen uit om een nieuwe Dataverse-omgeving te maken in dezelfde Active Directory-tenant:</span><span class="sxs-lookup"><span data-stu-id="31f74-129">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com/), and follow these steps to create a new Dataverse environment in the same Active Directory tenant:</span></span>

    1. <span data-ttu-id="31f74-130">Open de pagina **Omgevingen**.</span><span class="sxs-lookup"><span data-stu-id="31f74-130">Open the **Environments** page.</span></span>

        <span data-ttu-id="31f74-131">[![Pagina Omgevingen](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span><span class="sxs-lookup"><span data-stu-id="31f74-131">[![Environments page](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span></span>

    2. <span data-ttu-id="31f74-132">Selecteer de Dataverse-omgeving die u hierboven hebt gemaakt en selecteer vervolgens **Instellingen**.</span><span class="sxs-lookup"><span data-stu-id="31f74-132">Select the Dataverse environment created above and then select **Settings**.</span></span>
    3. <span data-ttu-id="31f74-133">Selecteer **Resources \> Alle oude instellingen**.</span><span class="sxs-lookup"><span data-stu-id="31f74-133">Select **Resources \> All Legacy Settings**.</span></span>
    4. <span data-ttu-id="31f74-134">Selecteer op de bovenste navigatiebalk **Instellingen** en vervolgens **Aanpassingen**.</span><span class="sxs-lookup"><span data-stu-id="31f74-134">On the top navigation bar, select **Settings**, and then select **Customizations**.</span></span>
    5. <span data-ttu-id="31f74-135">Selecteer **Resources voor ontwikkelaars**.</span><span class="sxs-lookup"><span data-stu-id="31f74-135">Select **Developer Resources**.</span></span>
    6. <span data-ttu-id="31f74-136">Kopieer de waarde van de **Dataverse-organisatie-id**.</span><span class="sxs-lookup"><span data-stu-id="31f74-136">Copy the **Dataverse organization ID** value.</span></span>
    7. <span data-ttu-id="31f74-137">Noteer de URL voor de Dataverse-organisatie in de adresbalk van de browser.</span><span class="sxs-lookup"><span data-stu-id="31f74-137">In the browser's address bar, make a note of the URL for the Dataverse organization.</span></span> <span data-ttu-id="31f74-138">De URL kan bijvoorbeeld `https://org42b2b3d3.crm.dynamics.com` zijn.</span><span class="sxs-lookup"><span data-stu-id="31f74-138">For example, the URL might be `https://org42b2b3d3.crm.dynamics.com`.</span></span>

3. <span data-ttu-id="31f74-139">Als u de functie Cashflowprognoses of Budgetprognoses wilt gebruiken, voert u de volgende stappen uit om de annotatielimiet voor uw organisatie bij te werken tot minimaal 50 MB:</span><span class="sxs-lookup"><span data-stu-id="31f74-139">If you plan to use the Cash flow forecasts or Budget forecasts feature, follow these steps to update the annotation limit for your organization to at least 50 megabytes (MB):</span></span>

    1. <span data-ttu-id="31f74-140">Open de [Power Apps-portal](https://make.powerapps.com).</span><span class="sxs-lookup"><span data-stu-id="31f74-140">Open the [Power Apps portal](https://make.powerapps.com).</span></span>
    2. <span data-ttu-id="31f74-141">Selecteer de omgeving die u zojuist hebt gemaakt en selecteer vervolgens **Geavanceerde instellingen**.</span><span class="sxs-lookup"><span data-stu-id="31f74-141">Select the environment that you just created, and then select **Advanced settings**.</span></span>
    3. <span data-ttu-id="31f74-142">Selecteer **Instellingen \> E-mailconfiguratie**.</span><span class="sxs-lookup"><span data-stu-id="31f74-142">Select **Settings \> Email Configuration**.</span></span>
    4. <span data-ttu-id="31f74-143">Wijzig de waarde van het veld **Maximale bestandsgrootte** in **51.200**.</span><span class="sxs-lookup"><span data-stu-id="31f74-143">Change the value of the **Maximum file size** field to **51,200**.</span></span> <span data-ttu-id="31f74-144">(De waarde wordt uitgedrukt in kilobytes \[KB\].)</span><span class="sxs-lookup"><span data-stu-id="31f74-144">(The value is expressed in kilobytes \[KB\].)</span></span>
    5. <span data-ttu-id="31f74-145">Selecteer **OK** om uw wijzigingen op te slaan.</span><span class="sxs-lookup"><span data-stu-id="31f74-145">Select **OK** to save your changes.</span></span>

## <a name="configure-the-azure-setup"></a><span data-ttu-id="31f74-146">De Azure-instellingen configureren</span><span class="sxs-lookup"><span data-stu-id="31f74-146">Configure the Azure setup</span></span>

### <a name="enter-the-dataverse-directory-id-and-the-users-azure-ad-object-id"></a><span data-ttu-id="31f74-147">De Dataverse-directory-id en de Azure AD-object-id van de gebruiker invoeren</span><span class="sxs-lookup"><span data-stu-id="31f74-147">Enter the Dataverse directory ID and the user's Azure AD object ID</span></span>

1. <span data-ttu-id="31f74-148">Voer de Dataverse-directory-id in:</span><span class="sxs-lookup"><span data-stu-id="31f74-148">Enter the Dataverse directory ID:</span></span>

    1. <span data-ttu-id="31f74-149">Open de [Azure Portal](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="31f74-149">Open the [Azure portal](https://portal.azure.com).</span></span>
    2. <span data-ttu-id="31f74-150">Meld u aan met de gebruikers-id die is gebruikt om de Dataverse-omgeving te maken.</span><span class="sxs-lookup"><span data-stu-id="31f74-150">Sign in by using the user ID that was used to create the Dataverse environment.</span></span>
    3. <span data-ttu-id="31f74-151">Ga naar **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="31f74-151">Go to **Azure Active Directory**.</span></span>
    4. <span data-ttu-id="31f74-152">Kopieer de waarde van de **Tenant-id**.</span><span class="sxs-lookup"><span data-stu-id="31f74-152">Copy the **Tenant ID** value.</span></span>

2. <span data-ttu-id="31f74-153">Voer de Azure Active Directory (Azure AD) object-id van de gebruiker in:</span><span class="sxs-lookup"><span data-stu-id="31f74-153">Enter the user's Azure Active Directory (Azure AD) object ID:</span></span>

    1. <span data-ttu-id="31f74-154">Ga in de [Azure-portal](https://portal.azure.com) naar **Gebruikers** en zoek de gebruiker op basis van het e-mailadres.</span><span class="sxs-lookup"><span data-stu-id="31f74-154">In the [Azure portal](https://portal.azure.com), go to **Users**, and search for the user by email address.</span></span>
    2. <span data-ttu-id="31f74-155">Selecteer de naam van de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="31f74-155">Select the user's name.</span></span>
    3. <span data-ttu-id="31f74-156">Kopieer de waarde van de **Object-id**.</span><span class="sxs-lookup"><span data-stu-id="31f74-156">Copy the **Object ID** value.</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="31f74-157">De Azure Cloud Shell gebruiken om Data Lake-resources voor Finance Insights in te stellen</span><span class="sxs-lookup"><span data-stu-id="31f74-157">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="31f74-158">Windows PowerShell-script gebruiken</span><span class="sxs-lookup"><span data-stu-id="31f74-158">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="31f74-159">Er is een Windows PowerShell-script meegeleverd, zodat u eenvoudig de Azure-resources kunt instellen die worden beschreven in de module [Export naar Azure Data Lake configureren](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="31f74-159">A Windows PowerShell script has been provided, so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span></span> <span data-ttu-id="31f74-160">Als u liever handmatig de instellingen opgeeft, slaat u deze procedure over en gaat u verder met de procedure in de sectie [Handmatige instellingen](#manual-setup).</span><span class="sxs-lookup"><span data-stu-id="31f74-160">If you prefer to do manual setup, skip this procedure, and continue with the procedure in the [Manual setup](#manual-setup) section.</span></span>

> [!NOTE]
> <span data-ttu-id="31f74-161">Voer de volgende stappen uit om het PowerShell-script uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="31f74-161">Follow the steps below to run the PowerShell script.</span></span> <span data-ttu-id="31f74-162">De Azure CLI-optie 'Probeer het' of het uitvoeren van het script op uw pc werkt mogelijk niet.</span><span class="sxs-lookup"><span data-stu-id="31f74-162">The Azure CLI "Try it" option, or running the script on your PC may not work.</span></span>

<span data-ttu-id="31f74-163">Voer de volgende stappen uit om Azure te configureren met het Windows PowerShell-script.</span><span class="sxs-lookup"><span data-stu-id="31f74-163">Follow these steps to configure Azure by using the Windows PowerShell script.</span></span> <span data-ttu-id="31f74-164">U moet beschikken over rechten om een Azure-resourcegroep, Azure-resources en een Azure AD-toepassing te maken.</span><span class="sxs-lookup"><span data-stu-id="31f74-164">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="31f74-165">Zie voor informatie over de vereiste machtigingen [Azure AD-machtigingen controleren](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span><span class="sxs-lookup"><span data-stu-id="31f74-165">For information about the required permissions, see [Check Azure AD permissions](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="31f74-166">Ga in de [Azure Portal](https://portal.azure.com) naar het Azure-abonnement van uw bestemming.</span><span class="sxs-lookup"><span data-stu-id="31f74-166">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span> <span data-ttu-id="31f74-167">Selecteer de knop **Cloud Shell** rechts van het veld **Zoeken**.</span><span class="sxs-lookup"><span data-stu-id="31f74-167">Select the **Cloud Shell** button to the right of the **Search** field.</span></span>
2. <span data-ttu-id="31f74-168">Selecteer **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="31f74-168">Select **PowerShell**.</span></span>
3. <span data-ttu-id="31f74-169">Maak opslagruimte als u hierom wordt gevraagd.</span><span class="sxs-lookup"><span data-stu-id="31f74-169">Create storage if you're prompted to do so.</span></span>
4. <span data-ttu-id="31f74-170">Ga naar het tabblad **Azure CLI** en selecteer **Kopiëren**.</span><span class="sxs-lookup"><span data-stu-id="31f74-170">Go to the **Azure CLI** tab and select **Copy**.</span></span>  
5. <span data-ttu-id="31f74-171">Open Kladblok en plak het PowerShell-script in een nieuw bestand.</span><span class="sxs-lookup"><span data-stu-id="31f74-171">Open Notepad and paste the PowerShell script.</span></span> <span data-ttu-id="31f74-172">Sla het bestand op met de naam ConfigureDataLake.ps1.</span><span class="sxs-lookup"><span data-stu-id="31f74-172">Save the file as ConfigureDataLake.ps1.</span></span>
6. <span data-ttu-id="31f74-173">Upload het Windows PowerShell-script naar de sessie via de menuoptie voor uploaden in Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="31f74-173">Upload the Windows PowerShell script to the session using the menu option for upload in Cloud Shell.</span></span>
7. <span data-ttu-id="31f74-174">Voer het script .\ConfigureDataLake.ps1 uit.</span><span class="sxs-lookup"><span data-stu-id="31f74-174">Run the script .\ConfigureDataLake.ps1.</span></span>
8. <span data-ttu-id="31f74-175">Volg de aanwijzingen om het script uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="31f74-175">Follow the prompts to run the script.</span></span>
9. <span data-ttu-id="31f74-176">Gebruik de informatie uit de scriptuitvoer om de invoegtoepassing **Exporteren naar Data Lake** in LCS te installeren.</span><span class="sxs-lookup"><span data-stu-id="31f74-176">Use the information from the script output to install the **Export to Data Lake** add-in in LCS.</span></span>
10. <span data-ttu-id="31f74-177">Gebruik de informatie uit de scriptuitvoer om de entiteitsopslag in te schakelen op de pagina **Gegevensverbindingen** in Financiën (**Systeembeheer \> Systeemparameters \> Gegevensverbindingen**).</span><span class="sxs-lookup"><span data-stu-id="31f74-177">Use the information from the script output to enable the entity store on the **Data connections** page in Finance (**System administration \> System parameters \> Data connections**).</span></span>

### <a name="manual-setup"></a><span data-ttu-id="31f74-178">Handmatige installatie</span><span class="sxs-lookup"><span data-stu-id="31f74-178">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="31f74-179">Toepassingen toevoegen aan de Azure AD-tenant</span><span class="sxs-lookup"><span data-stu-id="31f74-179">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="31f74-180">Ga in de [Azure Portal](https://portal.azure.com) naar **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="31f74-180">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="31f74-181">Selecteer **Beheren \> Ondernemingstoepassingen**.</span><span class="sxs-lookup"><span data-stu-id="31f74-181">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="31f74-182">Zoek naar de volgende toepassingen op app-id.</span><span class="sxs-lookup"><span data-stu-id="31f74-182">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="31f74-183">Sollicitatie</span><span class="sxs-lookup"><span data-stu-id="31f74-183">Application</span></span>                              | <span data-ttu-id="31f74-184">App-id</span><span class="sxs-lookup"><span data-stu-id="31f74-184">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="31f74-185">Microsoft Dynamics ERP-microservices</span><span class="sxs-lookup"><span data-stu-id="31f74-185">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="31f74-186">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="31f74-186">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="31f74-187">Microsoft Dynamics ERP-microservices CDS</span><span class="sxs-lookup"><span data-stu-id="31f74-187">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="31f74-188">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="31f74-188">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="31f74-189">AI Builder-autorisatieservice</span><span class="sxs-lookup"><span data-stu-id="31f74-189">AI Builder Authorization Service</span></span>         | <span data-ttu-id="31f74-190">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="31f74-190">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="31f74-191">Als u geen van de voorgaande toepassingen kunt vinden, voert u de volgende stappen uit.</span><span class="sxs-lookup"><span data-stu-id="31f74-191">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="31f74-192">Selecteer op uw lokale computer het menu **Start** en zoek naar **powershell**.</span><span class="sxs-lookup"><span data-stu-id="31f74-192">On your local machine, select the **Start** menu, and search for **powershell**.</span></span>
2. <span data-ttu-id="31f74-193">Selecteer **Windows PowerShell** en houd ingedrukt (of klik met de rechtermuisknop) en selecteer **Uitvoeren als beheerder**.</span><span class="sxs-lookup"><span data-stu-id="31f74-193">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="31f74-194">Voer de volgende opdracht uit om de **AzureAD**-module te installeren.</span><span class="sxs-lookup"><span data-stu-id="31f74-194">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="31f74-195">Als een NuGet-provider vereist is om door te gaan, selecteert u **J** om deze te installeren.</span><span class="sxs-lookup"><span data-stu-id="31f74-195">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="31f74-196">Als het bericht 'Niet-vertrouwde opslagplaats' wordt weergegeven, selecteert u **J** om door te gaan.</span><span class="sxs-lookup"><span data-stu-id="31f74-196">If an "Untrusted repository" message appears, select **Y** to continue.</span></span>
6. <span data-ttu-id="31f74-197">Voer voor elke toepassing die moet worden toegevoegd de volgende opdrachten uit om de toepassing toe te voegen aan Azure AD.</span><span class="sxs-lookup"><span data-stu-id="31f74-197">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="31f74-198">Meld u aan als Azure AD-beheerder als dat wordt gevraagd.</span><span class="sxs-lookup"><span data-stu-id="31f74-198">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="31f74-199">Azure-resources maken</span><span class="sxs-lookup"><span data-stu-id="31f74-199">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="31f74-200">Zorg ervoor dat u de volgende resources in hetzelfde Azure AD-exemplaar maakt als de Dataverse-omgeving.</span><span class="sxs-lookup"><span data-stu-id="31f74-200">Make sure that you create the following resources in the same Azure AD instance as the Dataverse environment.</span></span> <span data-ttu-id="31f74-201">U kunt resources uit een ander Azure AD-exemplaar niet gebruiken.</span><span class="sxs-lookup"><span data-stu-id="31f74-201">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="31f74-202">Een nieuw opslagaccount maken:</span><span class="sxs-lookup"><span data-stu-id="31f74-202">Create a new storage account:</span></span>

    1. <span data-ttu-id="31f74-203">Maak een opslag account in de [Azure Portal](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="31f74-203">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="31f74-204">Stel in het dialoogvenster **Opslagaccount maken** de volgende velden in:</span><span class="sxs-lookup"><span data-stu-id="31f74-204">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="31f74-205">**Locatie**: selecteer het datacentrum waar uw omgeving zich bevindt.</span><span class="sxs-lookup"><span data-stu-id="31f74-205">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="31f74-206">**Prestaties**: we raden u aan om **Standaard** te selecteren.</span><span class="sxs-lookup"><span data-stu-id="31f74-206">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="31f74-207">**Soort account**: selecteer **StorageV2**.</span><span class="sxs-lookup"><span data-stu-id="31f74-207">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="31f74-208">Selecteer **Inschakelen** onder **Hiërarchische naamruimten** in het dialoogvenster **Geavanceerde opties** voor de optie **Data Lake Storage Gen2**.</span><span class="sxs-lookup"><span data-stu-id="31f74-208">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="31f74-209">Als u deze functie uitschakelt, kunt u geen gegevens gebruiken die door Finance and Operations-apps worden geschreven met behulp van services zoals Power BI-gegevensstromen.</span><span class="sxs-lookup"><span data-stu-id="31f74-209">If you disable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="31f74-210">Selecteer **Controleren en maken**.</span><span class="sxs-lookup"><span data-stu-id="31f74-210">Select **Review and create**.</span></span> <span data-ttu-id="31f74-211">Wanneer de implementatie is voltooid, wordt de nieuwe resource weergegeven in de Azure Portal.</span><span class="sxs-lookup"><span data-stu-id="31f74-211">When the deployment is completed, the new resource will be shown in the Azure portal.</span></span>
    5. <span data-ttu-id="31f74-212">Ga naar het opslagaccount dat u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="31f74-212">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="31f74-213">Selecteer **Toegangssleutels** in het linkermenu.</span><span class="sxs-lookup"><span data-stu-id="31f74-213">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="31f74-214">Kopieer de verbindingstekenreeks en sla deze op voor **Key1** of **Key2**.</span><span class="sxs-lookup"><span data-stu-id="31f74-214">Copy and save the connection string for either **Key1** or **Key2**.</span></span>
    8. <span data-ttu-id="31f74-215">Kopieer de naam van het opslagaccount en sla deze op.</span><span class="sxs-lookup"><span data-stu-id="31f74-215">Copy and save the storage account name.</span></span>

2. <span data-ttu-id="31f74-216">Een Key Vault maken:</span><span class="sxs-lookup"><span data-stu-id="31f74-216">Create a new key vault:</span></span>

    1. <span data-ttu-id="31f74-217">Maak een Key Vault in de [Azure Portal](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="31f74-217">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="31f74-218">Selecteer in het dialoogvenster **Key Vault maken** in het veld **Locatie** het datacentrum waar uw omgeving zich bevindt.</span><span class="sxs-lookup"><span data-stu-id="31f74-218">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="31f74-219">Nadat de Key Vault is gemaakt, selecteert u deze in de lijst en selecteert u **Geheimen**.</span><span class="sxs-lookup"><span data-stu-id="31f74-219">After key vault is created, select it in the list, and then select **Secrets**.</span></span>
    4. <span data-ttu-id="31f74-220">Selecteer **Genereren/Importeren**.</span><span class="sxs-lookup"><span data-stu-id="31f74-220">Select **Generate/Import**.</span></span>
    5. <span data-ttu-id="31f74-221">Selecteer in het dialoogvenster **Een geheim maken** in het veld **Opties voor uploaden** de optie **Handmatig**.</span><span class="sxs-lookup"><span data-stu-id="31f74-221">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
    6. <span data-ttu-id="31f74-222">Voer een naam voor het geheim in.</span><span class="sxs-lookup"><span data-stu-id="31f74-222">Enter a name for the secret.</span></span> <span data-ttu-id="31f74-223">Noteer de naam, omdat u deze later moet opgeven.</span><span class="sxs-lookup"><span data-stu-id="31f74-223">Make a note of the name, because you will have to provide it later.</span></span>
    7. <span data-ttu-id="31f74-224">Voer in het veld **Waarde** de verbindingsreeks in die u hebt verkregen uit het opslagaccount in de vorige procedure.</span><span class="sxs-lookup"><span data-stu-id="31f74-224">In the **Value** field, enter the connection string that you obtained from the storage account in the previous procedure.</span></span>
    8. <span data-ttu-id="31f74-225">Selecteer **Ingeschakeld** en vervolgens **Maken**.</span><span class="sxs-lookup"><span data-stu-id="31f74-225">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="31f74-226">Het geheim wordt gemaakt en toegevoegd aan Key Vault.</span><span class="sxs-lookup"><span data-stu-id="31f74-226">The secret is created and added to Key Vault.</span></span>
    9. <span data-ttu-id="31f74-227">Ga naar **Overzicht van Key Vault** en noteer de DNS-naam.</span><span class="sxs-lookup"><span data-stu-id="31f74-227">Go to the **Key Vault Overview**, and make a note of the DNS name.</span></span>

3. <span data-ttu-id="31f74-228">Een Azure AD-toepassing maken en registreren:</span><span class="sxs-lookup"><span data-stu-id="31f74-228">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="31f74-229">Ga in de [Azure Portal](https://portal.azure.com) naar **Azure Active Directory** en selecteer **App-registraties**.</span><span class="sxs-lookup"><span data-stu-id="31f74-229">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="31f74-230">Selecteer **Nieuwe toepassingsregistratie** en stel de volgende velden in:</span><span class="sxs-lookup"><span data-stu-id="31f74-230">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="31f74-231">**Naam**: voer de naam van de app in.</span><span class="sxs-lookup"><span data-stu-id="31f74-231">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="31f74-232">**Toepassingstype**: selecteer **Web-API**.</span><span class="sxs-lookup"><span data-stu-id="31f74-232">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="31f74-233">**Omleidings-URL instellen**: voer de URL in voor uw Dynamics 365-exemplaar, bijvoorbeeld,`https://yourdynamicsinstance.dynamics.com/auth`.</span><span class="sxs-lookup"><span data-stu-id="31f74-233">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as, `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="31f74-234">Ga naar de app die u zojuist hebt gemaakt om de waarde van de **Toepassings-id (client)** te kopiëren en op te slaan.</span><span class="sxs-lookup"><span data-stu-id="31f74-234">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="31f74-235">Wanneer u de Key Vault instelt, moet u deze waarde later opgeven.</span><span class="sxs-lookup"><span data-stu-id="31f74-235">You will have to provide this value later, when you set up the key vault.</span></span>
    4. <span data-ttu-id="31f74-236">Ga naar **API-machtigingen** en voer de volgende stappen uit:</span><span class="sxs-lookup"><span data-stu-id="31f74-236">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="31f74-237">Selecteer **Een machtiging toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="31f74-237">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="31f74-238">Selecteer **Azure Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="31f74-238">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="31f74-239">Nadat u gedelegeerde machtigingen hebt geselecteerd, selecteert u **gebruikers\_imitatie**.</span><span class="sxs-lookup"><span data-stu-id="31f74-239">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="31f74-240">Selecteer **Machtigingen toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="31f74-240">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="31f74-241">Selecteer in het menu voor de app **Certificaten \& geheimen** en voer de volgende stappen uit om Key Vault-geheimen te maken:</span><span class="sxs-lookup"><span data-stu-id="31f74-241">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="31f74-242">Selecteer **Nieuw clientgeheim**.</span><span class="sxs-lookup"><span data-stu-id="31f74-242">Select **New client secret**.</span></span>
        2. <span data-ttu-id="31f74-243">Voer in het veld **Sleutelbeschrijving** een naam in.</span><span class="sxs-lookup"><span data-stu-id="31f74-243">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="31f74-244">Selecteer een duur en vervolgens **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="31f74-244">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="31f74-245">Er wordt een geheim gegenereerd in het veld **Waarde**.</span><span class="sxs-lookup"><span data-stu-id="31f74-245">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="31f74-246">Kopieer de geheime waarde en sla deze op.</span><span class="sxs-lookup"><span data-stu-id="31f74-246">Copy and save the secret value.</span></span>

4. <span data-ttu-id="31f74-247">Key Vault-geheimen maken:</span><span class="sxs-lookup"><span data-stu-id="31f74-247">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="31f74-248">Ga naar de Key Vault die u eerder hebt gemaakt en selecteer **Geheimen**.</span><span class="sxs-lookup"><span data-stu-id="31f74-248">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="31f74-249">Voer de volgende stappen uit voor elke geheime naam in de onderstaande tabel:</span><span class="sxs-lookup"><span data-stu-id="31f74-249">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="31f74-250">Selecteer **Genereren/Importeren**.</span><span class="sxs-lookup"><span data-stu-id="31f74-250">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="31f74-251">Selecteer in het dialoogvenster **Een geheim maken** in het veld **Opties voor uploaden** de optie **Handmatig**.</span><span class="sxs-lookup"><span data-stu-id="31f74-251">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="31f74-252">Maak de geheime naam en waarde uit de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="31f74-252">Create the secret name and value from the following table.</span></span>
        4. <span data-ttu-id="31f74-253">Selecteer **Ingeschakeld** en vervolgens **Maken**.</span><span class="sxs-lookup"><span data-stu-id="31f74-253">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="31f74-254">Het geheim wordt gemaakt en toegevoegd aan Key Vault.</span><span class="sxs-lookup"><span data-stu-id="31f74-254">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="31f74-255">Geheime naam</span><span class="sxs-lookup"><span data-stu-id="31f74-255">Secret name</span></span>                       | <span data-ttu-id="31f74-256">Geheime waarde</span><span class="sxs-lookup"><span data-stu-id="31f74-256">Secret value</span></span>                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | <span data-ttu-id="31f74-257">app-id</span><span class="sxs-lookup"><span data-stu-id="31f74-257">app-id</span></span>                            | <span data-ttu-id="31f74-258">De app-id van de toepassing die u eerder hebt gemaakt</span><span class="sxs-lookup"><span data-stu-id="31f74-258">The app ID of the application that you created earlier</span></span>                                      |
        | <span data-ttu-id="31f74-259">app-secret</span><span class="sxs-lookup"><span data-stu-id="31f74-259">app-secret</span></span>                        | <span data-ttu-id="31f74-260">Het clientgeheim dat u eerder hebt opgeslagen</span><span class="sxs-lookup"><span data-stu-id="31f74-260">The client secret that you saved earlier</span></span>                                                    |
        | <span data-ttu-id="31f74-261">storage-account-name</span><span class="sxs-lookup"><span data-stu-id="31f74-261">storage-account-name</span></span>              | <span data-ttu-id="31f74-262">De naam van het opslagaccount dat u eerder hebt gemaakt, zoals **storageaccount1**</span><span class="sxs-lookup"><span data-stu-id="31f74-262">The name of the storage account that you created earlier, such as **storageaccount1**</span></span>       |
        | <span data-ttu-id="31f74-263">storage-account-connection-string</span><span class="sxs-lookup"><span data-stu-id="31f74-263">storage-account-connection-string</span></span> | <span data-ttu-id="31f74-264">De verbindingsreeks die u van de pagina **Toegangssleutels** voor het opslagaccount hebt gekopieerd</span><span class="sxs-lookup"><span data-stu-id="31f74-264">The connection string that you copied from the **Access keys** page for the storage account</span></span> |

5. <span data-ttu-id="31f74-265">De toepassing machtigen om toegang te krijgen tot de Key Vault:</span><span class="sxs-lookup"><span data-stu-id="31f74-265">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="31f74-266">Open in de [Azure Portal](https://portal.azure.com) de Key Vault die u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="31f74-266">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="31f74-267">Selecteer het toegangsbeleid.</span><span class="sxs-lookup"><span data-stu-id="31f74-267">Select the access policies.</span></span>
    3. <span data-ttu-id="31f74-268">Voer de volgende stappen uit voor elke toepassing in de onderstaande tabel:</span><span class="sxs-lookup"><span data-stu-id="31f74-268">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="31f74-269">Selecteer **Toegangsbeleid toevoegen** om een toegangsbeleid te maken.</span><span class="sxs-lookup"><span data-stu-id="31f74-269">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="31f74-270">Selecteer in het veld **Geheime machtigingen** de machtigingen uit de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="31f74-270">In the **Secret permissions** field, select the permissions from the following table.</span></span>
        3. <span data-ttu-id="31f74-271">Zoek in het veld **Principal selecteren** de weergavenaam van de toepassing uit de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="31f74-271">In the **Select principal** field, search for the application display name from the following table.</span></span>
        4. <span data-ttu-id="31f74-272">Selecteer **Selecteren**.</span><span class="sxs-lookup"><span data-stu-id="31f74-272">Select **Select**.</span></span>
        5. <span data-ttu-id="31f74-273">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="31f74-273">Select **Add**.</span></span>
        6. <span data-ttu-id="31f74-274">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="31f74-274">Select **Save**.</span></span>

        | <span data-ttu-id="31f74-275">Sollicitatie</span><span class="sxs-lookup"><span data-stu-id="31f74-275">Application</span></span>                                              | <span data-ttu-id="31f74-276">Machtigingen</span><span class="sxs-lookup"><span data-stu-id="31f74-276">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="31f74-277">De weergavenaam van de nieuwe toepassing die u hebt gemaakt</span><span class="sxs-lookup"><span data-stu-id="31f74-277">The display name of the new application that you created</span></span> | <span data-ttu-id="31f74-278">Ophalen, Lijst</span><span class="sxs-lookup"><span data-stu-id="31f74-278">Get, List</span></span>   |
        | <span data-ttu-id="31f74-279">**Microsoft Dynamics ERP-microservices**</span><span class="sxs-lookup"><span data-stu-id="31f74-279">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="31f74-280">Ophalen, Lijst</span><span class="sxs-lookup"><span data-stu-id="31f74-280">Get, List</span></span>   |

6. <span data-ttu-id="31f74-281">Rollen toewijzen voor toegang tot het opslagaccount:</span><span class="sxs-lookup"><span data-stu-id="31f74-281">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="31f74-282">Open in de [Azure Portal](https://portal.azure.com) het opslagaccount dat u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="31f74-282">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="31f74-283">Selecteer **Access Control (IAM)** en vervolgens **Roltoewijzingen**.</span><span class="sxs-lookup"><span data-stu-id="31f74-283">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="31f74-284">Selecteer **Toevoegen, Roltoewijzing toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="31f74-284">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="31f74-285">Voer de volgende stappen uit voor elke toepassing in de onderstaande tabel:</span><span class="sxs-lookup"><span data-stu-id="31f74-285">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="31f74-286">Selecteer de rol in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="31f74-286">Select the role from the following table.</span></span>
        2. <span data-ttu-id="31f74-287">Laat het veld **Toegang toewijzen aan** ingesteld staan op **Azure AD-gebruiker, -groep of serviceprincipal**.</span><span class="sxs-lookup"><span data-stu-id="31f74-287">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="31f74-288">Voer in het veld **Selecteren** de toepassing uit de volgende tabel in.</span><span class="sxs-lookup"><span data-stu-id="31f74-288">In the **Select** field, enter the application from the following table.</span></span>
        4. <span data-ttu-id="31f74-289">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="31f74-289">Select **Save**.</span></span>

        | <span data-ttu-id="31f74-290">Sollicitatie</span><span class="sxs-lookup"><span data-stu-id="31f74-290">Application</span></span>                                              | <span data-ttu-id="31f74-291">Rol</span><span class="sxs-lookup"><span data-stu-id="31f74-291">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="31f74-292">De weergavenaam van de nieuwe toepassing die u hebt gemaakt</span><span class="sxs-lookup"><span data-stu-id="31f74-292">The display name of the new application that you created</span></span> | <span data-ttu-id="31f74-293">Eigenaar</span><span class="sxs-lookup"><span data-stu-id="31f74-293">Owner</span></span>                       |
        | <span data-ttu-id="31f74-294">De weergavenaam van de nieuwe toepassing die u hebt gemaakt</span><span class="sxs-lookup"><span data-stu-id="31f74-294">The display name of the new application that you created</span></span> | <span data-ttu-id="31f74-295">Inzender</span><span class="sxs-lookup"><span data-stu-id="31f74-295">Contributor</span></span>                 |
        | <span data-ttu-id="31f74-296">De weergavenaam van de nieuwe toepassing die u hebt gemaakt</span><span class="sxs-lookup"><span data-stu-id="31f74-296">The display name of the new application that you created</span></span> | <span data-ttu-id="31f74-297">Inzender voor opslagaccounts</span><span class="sxs-lookup"><span data-stu-id="31f74-297">Storage Account Contributor</span></span> |
        | <span data-ttu-id="31f74-298">De weergavenaam van de nieuwe toepassing die u hebt gemaakt</span><span class="sxs-lookup"><span data-stu-id="31f74-298">The display name of the new application that you created</span></span> | <span data-ttu-id="31f74-299">Eigenaar van gegevens in opslagblob</span><span class="sxs-lookup"><span data-stu-id="31f74-299">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="31f74-300">**AI Builder-autorisatieservice**</span><span class="sxs-lookup"><span data-stu-id="31f74-300">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="31f74-301">Lezer van gegevens in opslagblob</span><span class="sxs-lookup"><span data-stu-id="31f74-301">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="31f74-302">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="31f74-302">Azure CLI</span></span>](#tab/azure-azure-cli)

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



## <a name="configure-the-data-lake"></a><span data-ttu-id="31f74-303">Het data lake configureren</span><span class="sxs-lookup"><span data-stu-id="31f74-303">Configure the data lake</span></span>

<span data-ttu-id="31f74-304">Voer de volgende stappen uit om de Azure Data Lake-invoegtoepassing aan de omgeving toe te voegen met LCS.</span><span class="sxs-lookup"><span data-stu-id="31f74-304">Follow these steps to use LCS to add the Azure Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="31f74-305">Meld u aan bij LCS en selecteer vervolgens **Volledige details** onder de naam van de omgeving aan de rechterkant van de pagina.</span><span class="sxs-lookup"><span data-stu-id="31f74-305">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="31f74-306">Selecteer in de sectie **Invoegtoepassingen voor omgeving** de optie **Een nieuwe invoegtoepassing installeren**.</span><span class="sxs-lookup"><span data-stu-id="31f74-306">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="31f74-307">Selecteer de invoegtoepassing **Exporteren naar Data Lake**.</span><span class="sxs-lookup"><span data-stu-id="31f74-307">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="31f74-308">Voer de volgende waarden in.</span><span class="sxs-lookup"><span data-stu-id="31f74-308">Enter the following values.</span></span>

    | <span data-ttu-id="31f74-309">Waarde</span><span class="sxs-lookup"><span data-stu-id="31f74-309">Value</span></span>                                                              | <span data-ttu-id="31f74-310">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="31f74-310">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="31f74-311">De tenant-id van het Azure-abonnement waarin de Key Vault zich bevindt</span><span class="sxs-lookup"><span data-stu-id="31f74-311">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="31f74-312">De tenant-id waar het opslagaccount, de apps en de key vaults zich bevinden.</span><span class="sxs-lookup"><span data-stu-id="31f74-312">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="31f74-313">Als u deze waarde wilt zoeken, opent u de [Azure Portal](https://portal.azure.com), gaat u naar **Azure Active Directory** en kopieert u de waarde van **Tenant-id**.</span><span class="sxs-lookup"><span data-stu-id="31f74-313">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="31f74-314">Geef de DNS-naam op van uw Key Vault</span><span class="sxs-lookup"><span data-stu-id="31f74-314">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="31f74-315">De DNS-naam van de Key Vault, zoals `https://customkeyvault.vault.azure.net/`.</span><span class="sxs-lookup"><span data-stu-id="31f74-315">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> <span data-ttu-id="31f74-316">(Deze waarde komt overeen met de DNS-naam die in de entiteitsopslag wordt gebruikt.)</span><span class="sxs-lookup"><span data-stu-id="31f74-316">(This value matches the DNS name that is used in the entity store.)</span></span> |
    | <span data-ttu-id="31f74-317">Het geheim opgeven dat de naam van het opslagaccount bevat</span><span class="sxs-lookup"><span data-stu-id="31f74-317">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="31f74-318">**storage-account-name**</span><span class="sxs-lookup"><span data-stu-id="31f74-318">**storage-account-name**</span></span> |
    | <span data-ttu-id="31f74-319">Geheime naam voor de app-ID die moet worden gebruikt voor toegang tot Data Lake</span><span class="sxs-lookup"><span data-stu-id="31f74-319">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="31f74-320">**app-id**</span><span class="sxs-lookup"><span data-stu-id="31f74-320">**app-id**</span></span> |
    | <span data-ttu-id="31f74-321">Geheime naam om te gebruiken met app-id</span><span class="sxs-lookup"><span data-stu-id="31f74-321">Secret name to be used with App ID</span></span>                                 | <span data-ttu-id="31f74-322">**app-secret**</span><span class="sxs-lookup"><span data-stu-id="31f74-322">**app-secret**</span></span> |

5. <span data-ttu-id="31f74-323">Ga akkoord met de voorwaarden en selecteer **Installeren**.</span><span class="sxs-lookup"><span data-stu-id="31f74-323">Agree to the terms, and select **Install**.</span></span>

<span data-ttu-id="31f74-324">De invoegtoepassing wordt binnen enkele minuten geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="31f74-324">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-ai-builder"></a><span data-ttu-id="31f74-325">AI Builder configureren</span><span class="sxs-lookup"><span data-stu-id="31f74-325">Configure AI Builder</span></span>

1. <span data-ttu-id="31f74-326">Meld u aan bij LCS en open de pagina **Omgevingsdetails**.</span><span class="sxs-lookup"><span data-stu-id="31f74-326">Sign in to LCS, and open the **Environment details** page.</span></span>
2. <span data-ttu-id="31f74-327">Schuif naar de sectie **Invoegtoepassingen voor omgeving**.</span><span class="sxs-lookup"><span data-stu-id="31f74-327">Scroll to the **Environment add-ins** section.</span></span> <span data-ttu-id="31f74-328">De invoegtoepassingen die al in deze omgeving zijn geïnstalleerd, worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="31f74-328">You should see the add-ins that are already installed in this environment.</span></span> <span data-ttu-id="31f74-329">Als de invoegtoepassing **Exporteren naar Data Lake** daar niet bij staat, configureert u deze invoegtoepassing.</span><span class="sxs-lookup"><span data-stu-id="31f74-329">If the **Export to Data Lake** add-in isn't among them, configure this add-in.</span></span>
3. <span data-ttu-id="31f74-330">Selecteer de invoegtoepassing **Inzichten downloaden**.</span><span class="sxs-lookup"><span data-stu-id="31f74-330">Select the **Get insights** add-in.</span></span>
4. <span data-ttu-id="31f74-331">Voer de volgende waarden in op de detailspagina van de invoegtoepassing **Inzichten downloaden**.</span><span class="sxs-lookup"><span data-stu-id="31f74-331">On the **Get insights** add-in details page, enter the following values.</span></span>

    | <span data-ttu-id="31f74-332">Waarde</span><span class="sxs-lookup"><span data-stu-id="31f74-332">Value</span></span>                                                    | <span data-ttu-id="31f74-333">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="31f74-333">Description</span></span> |
    |----------------------------------------------------------|-------------|
    | <span data-ttu-id="31f74-334">Organisatie-URL CDS</span><span class="sxs-lookup"><span data-stu-id="31f74-334">CDS Organization URL</span></span>                                     | <span data-ttu-id="31f74-335">De URL van de Dataverse-organisatie die u hierboven hebt gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="31f74-335">The Dataverse organization URL copied from above.</span></span> |
    | <span data-ttu-id="31f74-336">CDS Org-id</span><span class="sxs-lookup"><span data-stu-id="31f74-336">CDS Org ID</span></span>                                               | <span data-ttu-id="31f74-337">De id van de Dataverse-organisatie die u hierboven hebt gekopieerd.</span><span class="sxs-lookup"><span data-stu-id="31f74-337">The Dataverse organization ID copied from above.</span></span> |
5. <span data-ttu-id="31f74-338">Schakel de optie **Is dit de standaard CDS-omgeving voor de tenant?** in.</span><span class="sxs-lookup"><span data-stu-id="31f74-338">Enable **Is this the default environment for you Tenant**.</span></span>
    
## <a name="configure-the-entity-store"></a><span data-ttu-id="31f74-339">De entiteitsopslag configureren</span><span class="sxs-lookup"><span data-stu-id="31f74-339">Configure the entity store</span></span>

<span data-ttu-id="31f74-340">Voer de volgende stappen uit om de entiteitsopslag in te stellen in uw Finance-omgeving.</span><span class="sxs-lookup"><span data-stu-id="31f74-340">Follow these steps to set up the entity store in your Finance environment.</span></span>

1. <span data-ttu-id="31f74-341">Ga naar **Systeembeheer \> Instellen \> Systeemparameters \> Gegevensverbindingen**.</span><span class="sxs-lookup"><span data-stu-id="31f74-341">Go to **System administration \> Setup \> System parameters \> Data connections**.</span></span>
2. <span data-ttu-id="31f74-342">Stel de volgende Key Vault-velden in:</span><span class="sxs-lookup"><span data-stu-id="31f74-342">Set the following key vault fields:</span></span>

    - <span data-ttu-id="31f74-343">**Toepassings-id (client)**: voer de id van de toepassingsclient in die u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="31f74-343">**Application (client) ID** – Enter the application client ID that you created earlier.</span></span>
    - <span data-ttu-id="31f74-344">**Toepassingsgeheim**: voer het geheim in dat u hebt opgeslagen voor de toepassing die u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="31f74-344">**Application Secret** – Enter the secret that you saved for the application that you created earlier.</span></span>
    - <span data-ttu-id="31f74-345">**DNS-naam**: u kunt de DNS-naam (Domain Name System) vinden op de pagina met toepassingsdetails voor de toepassing die u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="31f74-345">**DNS name** – You can find the Domain Name System (DNS) name on the application details page for the application that you created earlier.</span></span>
    - <span data-ttu-id="31f74-346">**Geheime naam**: voer een **storage-account-connection-string** in.</span><span class="sxs-lookup"><span data-stu-id="31f74-346">**Secret name** – Enter **storage-account-connection-string**.</span></span>
3. <span data-ttu-id="31f74-347">Schakel **Data Lake-integratie inschakelen** in.</span><span class="sxs-lookup"><span data-stu-id="31f74-347">Enable **Enable Data Lake integration**.</span></span>
4. <span data-ttu-id="31f74-348">Selecteer **Azure Key Vault testen** en controleer of er fouten worden gemeld.</span><span class="sxs-lookup"><span data-stu-id="31f74-348">Select **Test Azure Key Vault** and verify there are no errors.</span></span>
5. <span data-ttu-id="31f74-349">Selecteer **Azure-opslag testen** en controleer of er fouten worden gemeld.</span><span class="sxs-lookup"><span data-stu-id="31f74-349">Select **Test Azure storage** and verify there are no errors.</span></span>

## <a name="feedback-and-support"></a><span data-ttu-id="31f74-350">Feedback en ondersteuning</span><span class="sxs-lookup"><span data-stu-id="31f74-350">Feedback and support</span></span>

<span data-ttu-id="31f74-351">Stuur een e-mail naar [Inzichten voor betalingen van klanten (preview)](mailto:fiap@microsoft.com) als u feedback wilt geven of ondersteuning nodig hebt.</span><span class="sxs-lookup"><span data-stu-id="31f74-351">Please send an email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in providing feedback or need support.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="31f74-352">Privacyverklaring</span><span class="sxs-lookup"><span data-stu-id="31f74-352">Privacy notice</span></span>

<span data-ttu-id="31f74-353">Previews (1) bieden mogelijk minder privacy- en beveiligingsmaatregelen dan de service Dynamics 365 Finance and Operations, (2) worden niet opgenomen in de serviceovereenkomst voor deze service, (3) mogen niet worden gebruikt voor de verwerking van persoonsgegevens of andere gegevens die aan juridische of wettelijke nalevingvereisten zijn onderworpen en (4) worden slechts beperkt ondersteund.</span><span class="sxs-lookup"><span data-stu-id="31f74-353">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
