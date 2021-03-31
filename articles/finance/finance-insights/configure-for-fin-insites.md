---
title: Configuratie voor Financiële inzichten (preview)
description: In dit onderwerp worden de configuratiestappen beschreven die ervoor zorgen dat uw systeem de mogelijkheden gebruikt die beschikbaar zijn in Financiële inzichten.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: cf29e3c05f9fdcc685017a4c640ef32c40989c73
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5208552"
---
# <a name="configuration-for-finance-insights-preview"></a><span data-ttu-id="f90b3-103">Configuratie voor Financiële inzichten (preview)</span><span class="sxs-lookup"><span data-stu-id="f90b3-103">Configuration for Finance insights (preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="f90b3-104">Financiële inzichten combineert de functionaliteit van Microsoft Dynamics 365 Finance met Microsoft Dataverse, Azure en AI Builder, zodat u beschikt over krachtige prognosefuncties voor uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="f90b3-104">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Microsoft Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="f90b3-105">In dit onderwerp worden de configuratiestappen beschreven die ervoor zorgen dat uw systeem de mogelijkheden gebruikt die beschikbaar zijn in Financiële inzichten.</span><span class="sxs-lookup"><span data-stu-id="f90b3-105">This topic explains the configuration steps that will enable your system to use the capabilities that are available in Finance insights.</span></span>

## <a name="deploy-dynamics-365-finance"></a><span data-ttu-id="f90b3-106">Dynamics 365 Finance implementeren</span><span class="sxs-lookup"><span data-stu-id="f90b3-106">Deploy Dynamics 365 Finance</span></span>

<span data-ttu-id="f90b3-107">Ga als volgt te werk om de omgevingen te implementeren.</span><span class="sxs-lookup"><span data-stu-id="f90b3-107">Deploy the environments by following these steps.</span></span>

1. <span data-ttu-id="f90b3-108">In Microsoft Dynamics Lifecycle Services (LCS) kunt u een Dynamics 365 Finance-omgeving maken of bijwerken.</span><span class="sxs-lookup"><span data-stu-id="f90b3-108">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Dynamics 365 Finance environment.</span></span> <span data-ttu-id="f90b3-109">Voor de omgeving is app-versie 10.0.11/Platform update 35 of hoger vereist.</span><span class="sxs-lookup"><span data-stu-id="f90b3-109">The environment requires app version 10.0.11/Platform update 35 or later.</span></span>
2. <span data-ttu-id="f90b3-110">De omgeving moet een omgeving met hoge beschikbaarheid (HA) zijn in de sandbox.</span><span class="sxs-lookup"><span data-stu-id="f90b3-110">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="f90b3-111">(Dit type omgeving wordt ook wel een Tier-2-omgeving genoemd.) Zie [Omgevingsplanning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="f90b3-111">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="f90b3-112">Als u Contoso-demogegevens gebruikt, hebt u aanvullende voorbeeldgegevens nodig om de functies Voorspellingen voor klantbetalingen, Cashflowprognoses en Budgetprognoses te gebruiken.</span><span class="sxs-lookup"><span data-stu-id="f90b3-112">If you're using Contoso demo data, you will require additional sample data to use the Customer payment predictions, Cash flow forecasts, and Budget forecasts features.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="f90b3-113">Dataverse configureren</span><span class="sxs-lookup"><span data-stu-id="f90b3-113">Configure Dataverse</span></span>

<span data-ttu-id="f90b3-114">U kunt de volgende handmatige configuratiestappen uitvoeren, of u kunt het configuratieproces versnellen met behulp van het Windows PowerShell-script dat wordt meegeleverd.</span><span class="sxs-lookup"><span data-stu-id="f90b3-114">You can complete the manual configuration steps that follow, or you can speed up the configuration process by using the Windows PowerShell script that is provided.</span></span> <span data-ttu-id="f90b3-115">Na het uitvoeren het PowerShell-script krijgt u waarden die u kunt gebruiken voor het configureren van Financiële inzichten.</span><span class="sxs-lookup"><span data-stu-id="f90b3-115">When the PowerShell script has finished running, it will give you values to use to configure Finance insights.</span></span> 

> [!NOTE]
> <span data-ttu-id="f90b3-116">Open PowerShell op de pc om het script uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="f90b3-116">Open PowerShell on your PC to run the script.</span></span> <span data-ttu-id="f90b3-117">U hebt mogelijk PowerShell versie 5 nodig.</span><span class="sxs-lookup"><span data-stu-id="f90b3-117">You may need PowerShell version 5.</span></span> <span data-ttu-id="f90b3-118">De Microsoft Azure Cli-optie 'Probeer het' werkt mogelijk niet.</span><span class="sxs-lookup"><span data-stu-id="f90b3-118">The Microsoft Azure CLI "Try it" option may not work.</span></span>

# <a name="manual-configuration-steps"></a>[<span data-ttu-id="f90b3-119">Handmatige configuratiestappen</span><span class="sxs-lookup"><span data-stu-id="f90b3-119">Manual configuration steps</span></span>](#tab/configuration-steps)

1. <span data-ttu-id="f90b3-120">Open het [Power Platform-beheercentrum](https://admin.powerplatform.microsoft.com/) en voer de volgende stappen uit om een nieuwe Dataverse-omgeving te maken in dezelfde Active Directory-tenant:</span><span class="sxs-lookup"><span data-stu-id="f90b3-120">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com/), and follow these steps to create a new Dataverse environment in the same Active Directory tenant:</span></span>

    1. <span data-ttu-id="f90b3-121">Open de pagina **Omgevingen**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-121">Open the **Environments** page.</span></span>

        <span data-ttu-id="f90b3-122">[![Pagina Omgevingen](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span><span class="sxs-lookup"><span data-stu-id="f90b3-122">[![Environments page](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span></span>

    2. <span data-ttu-id="f90b3-123">Selecteer **Nieuwe omgeving**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-123">Select **New environment**.</span></span>
    3. <span data-ttu-id="f90b3-124">Selecteer **Sandbox** in het veld **Type**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-124">In the **Type** field, select **Sandbox**.</span></span>
    4. <span data-ttu-id="f90b3-125">Stel de optie **Database maken** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-125">Set the **Create Database** option to **Yes**.</span></span>
    5. <span data-ttu-id="f90b3-126">Selecteer **Volgende**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-126">Select **Next**.</span></span>
    6. <span data-ttu-id="f90b3-127">Selecteer de taal en valuta voor uw organisatie.</span><span class="sxs-lookup"><span data-stu-id="f90b3-127">Select the language and currency for your organization.</span></span>
    7. <span data-ttu-id="f90b3-128">Accepteer de standaardwaarden voor de overige velden.</span><span class="sxs-lookup"><span data-stu-id="f90b3-128">Accept the default values for the other fields.</span></span>
    8. <span data-ttu-id="f90b3-129">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-129">Select **Save**.</span></span>
    9. <span data-ttu-id="f90b3-130">Vernieuw de pagina **Omgevingen**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-130">Refresh the **Environments** page.</span></span>
    10. <span data-ttu-id="f90b3-131">Wacht totdat de waarde van het veld **Status** is bijgewerkt naar **Gereed**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-131">Wait until the value of the **State** field is updated to **Ready**.</span></span>
    11. <span data-ttu-id="f90b3-132">Noteer de id van de Dataverse-organisatie.</span><span class="sxs-lookup"><span data-stu-id="f90b3-132">Make a note of the Dataverse organization ID.</span></span>
    12. <span data-ttu-id="f90b3-133">Selecteer de omgeving en selecteer vervolgens **Instellingen**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-133">Select the environment, and then select **Settings**.</span></span>
    13. <span data-ttu-id="f90b3-134">Selecteer **Resources \> Alle oude instellingen**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-134">Select **Resources \> All Legacy Settings**.</span></span>
    14. <span data-ttu-id="f90b3-135">Selecteer op de bovenste navigatiebalk **Instellingen** en vervolgens **Aanpassingen**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-135">On the top navigation bar, select **Settings**, and then select **Customizations**.</span></span>
    15. <span data-ttu-id="f90b3-136">Selecteer **Resources voor ontwikkelaars**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-136">Select **Developer Resources**.</span></span>
    16. <span data-ttu-id="f90b3-137">Stel het veld **Id van verwijzingsgegevens van exemplaar** in op de id van de Dataverse-organisatie die u eerder hebt genoteerd.</span><span class="sxs-lookup"><span data-stu-id="f90b3-137">Set the **Instance Reference Information ID** field to the Dataverse organization ID value that you made a note of earlier.</span></span>
    17. <span data-ttu-id="f90b3-138">Noteer de URL voor de Dataverse-organisatie in de adresbalk van de browser.</span><span class="sxs-lookup"><span data-stu-id="f90b3-138">In the browser's address bar, make a note of the URL for the Dataverse organization.</span></span> <span data-ttu-id="f90b3-139">De URL kan bijvoorbeeld `https://org42b2b3d3.crm.dynamics.com` zijn.</span><span class="sxs-lookup"><span data-stu-id="f90b3-139">For example, the URL might be `https://org42b2b3d3.crm.dynamics.com`.</span></span>

2. <span data-ttu-id="f90b3-140">Als u de functie Cashflowprognoses of Budgetprognoses wilt gebruiken, voert u de volgende stappen uit om de annotatielimiet voor uw organisatie bij te werken tot minimaal 50 MB:</span><span class="sxs-lookup"><span data-stu-id="f90b3-140">If you plan to use the Cash flow forecasts or Budget forecasts feature, follow these steps to update the annotation limit for your organization to at least 50 megabytes (MB):</span></span>

    1. <span data-ttu-id="f90b3-141">Open de [Power Apps-portal](https://make.powerapps.com).</span><span class="sxs-lookup"><span data-stu-id="f90b3-141">Open the [Power Apps portal](https://make.powerapps.com).</span></span>
    2. <span data-ttu-id="f90b3-142">Selecteer de omgeving die u zojuist hebt gemaakt en selecteer vervolgens **Geavanceerde instellingen**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-142">Select the environment that you just created, and then select **Advanced settings**.</span></span>
    3. <span data-ttu-id="f90b3-143">Selecteer **Instellingen \> E-mailconfiguratie**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-143">Select **Settings \> Email Configuration**.</span></span>
    4. <span data-ttu-id="f90b3-144">Wijzig de waarde van het veld **Maximale bestandsgrootte** in **51.200**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-144">Change the value of the **Maximum file size** field to **51,200**.</span></span> <span data-ttu-id="f90b3-145">(De waarde wordt uitgedrukt in kilobytes \[KB\].)</span><span class="sxs-lookup"><span data-stu-id="f90b3-145">(The value is expressed in kilobytes \[KB\].)</span></span>
    5. <span data-ttu-id="f90b3-146">Selecteer **OK** om uw wijzigingen op te slaan.</span><span class="sxs-lookup"><span data-stu-id="f90b3-146">Select **OK** to save your changes.</span></span>

# <a name="windows-powershell-configuration-script"></a>[<span data-ttu-id="f90b3-147">Windows PowerShell-configuratiescript</span><span class="sxs-lookup"><span data-stu-id="f90b3-147">Windows PowerShell configuration script</span></span>](#tab/powershell-configuration-script)

```azurecli-interactive
Write-Output 'The following modules need to be present for execution of this script:'
Write-Output '  Microsoft.PowerApps.Administration.PowerShell'
Write-Output '  Microsoft.PowerApps.PowerShell'
Write-Output '  Microsoft.Xrm.Tooling.CrmConnector.PowerShell'

try {
    $moduleConsent = Read-Host 'Is it ok to install or update these modules as needed? (yes/no)'
    if ($moduleConsent -ne 'yes' -and $moduleConsent -ne 'y') {
        Write-Warning 'User declined to install required modules.'
        return
    }

    $module = 'Microsoft.PowerApps.Administration.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '2.0.61' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '2.0.61' -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    $module = 'Microsoft.PowerApps.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '1.0.9' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '1.0.9' -AllowClobber -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    $module = 'Microsoft.Xrm.Tooling.CrmConnector.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '3.3.0.892' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '3.3.0.892' -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    Write-Output '================================================================================='

    $useMfa = $false
    $useMfaPrompt = Read-Host "Does your organization require the use of multi-factor authentication? (yes/no)"
    if ($useMfaPrompt -eq 'yes' -or $useMfaPrompt -eq 'y') {
        $useMfa = $true
    }
    if(-not $useMfa) {
        $credential = Get-Credential -Message 'Power Apps Credential'
    }

    $orgFriendlyName = Read-Host "Enter the name of the CDS Organization to use or create: (blank for 'FinanceInsightsOrg')"
    if ($orgFriendlyName.Trim() -eq '') {
        $orgFriendlyName = 'FinanceInsightsOrg'
    }

    $isDefaultOrgPrompt = Read-Host ("Is '" + $orgFriendlyName + "' the default organization for your tenant? (yes/no)")
    if ($isDefaultOrgPrompt -eq 'yes' -or $isDefaultOrgPrompt -eq 'y') {
        $isDefaultOrg = $true
    }

    if ($credential) {
        Add-PowerAppsAccount -Username $credential.UserName -Password $credential.Password
    }
    else {
        Add-PowerAppsAccount
    }

    if ($isDefaultOrg) {
        $orgMatch = ('(default)')
        $environment = (Get-AdminPowerAppEnvironment | Where-Object { $_.IsDefault -eq $true })
    }
    else {
        $orgMatch = ('{0} (*)' -f $orgFriendlyName)
        $environment = (Get-AdminPowerAppEnvironment | Where-Object { ($_.IsDefault -eq $false -and ($_.DisplayName -eq $orgFriendlyName -or $_.DisplayName -like $orgMatch)) })
    }

    $getCrmOrgParams = @{ 'OnlineType' = 'Office365' }
    if ($credential) {
        $getCrmOrgParams.Credential = $credential
    }

    if ($null -eq $environment) {
        Write-Output '================================================================================='
        Write-Output 'PowerApps environment not found. A new one will be provisioned.'

        $invalid = 'invalid'

        $location = $invalid
        $cdsLocations = (Get-AdminPowerAppEnvironmentLocations | Select-Object LocationName).LocationName
        while (-not ($location -in $cdsLocations)) {
            $location = (Read-Host -Prompt "Enter the location in which to create the new PowerApps environment: ('help' to see values)")
            if ($location -eq 'help') {
                $cdsLocations
            }
        }

        $currency = $invalid
        $cdsCurrencies = (Get-AdminPowerAppCdsDatabaseCurrencies -Location $location | Select-Object CurrencyName).CurrencyName
        while ($currency -ne '' -and -not ($currency -in $cdsCurrencies)) {
            $currency = (Read-Host -Prompt "Enter the currency to use for the new PowerApps environment: ('help' to see values, blank for default)")
            if ($currency -eq 'help') {
                $cdsCurrencies
            }
        }

        $language = $invalid
        $cdsLanguages = (Get-AdminPowerAppCdsDatabaseLanguages -Location $location | Select-Object LanguageName, LanguageDisplayName)
        while ($language -ne '' -and -not ($language -in $cdsLanguages.LanguageName)) {
            $language = (Read-Host -Prompt "Enter the language name to use for the new PowerApps environment: ('help' to see values, blank for default)")
            if ($language -eq 'help') {
                $cdsLanguages | Format-Table -Property LanguageName, LanguageDisplayName
            }
        }

        Write-Output 'Provisioning PowerApps environment. This may take several minutes.'

        $sleep = 15

        $envParams = @{ 'DisplayName' = $orgFriendlyName; 'EnvironmentSku' = 'Sandbox'; 'ProvisionDatabase' = $true; 'Location' = $location; 'WaitUntilFinished' = $true }
        if ($language.Trim() -ne '') {
            $envParams.LanguageName = $language
        }
        if ($currency.Trim() -ne '') {
            $envParams.CurrencyName = $currency
        }
        $newEnvResult = New-AdminPowerAppEnvironment @envParams
        if (($null -eq $newEnvResult) -or ($newEnvResult.CommonDataServiceDatabaseProvisioningState -ne 'Succeeded')) {
            Write-Warning 'Failed to create to PowerApps environment'
            if ($null -ne $newEnvResult) {
                $newEnvResult
            }
        }
        else {
            $environment = $null
            $retryCount = 0
            while (($null -eq $environment) -and ($retryCount -lt 5)) {
                Start-Sleep -Seconds $sleep
                $environment = (Get-AdminPowerAppEnvironment | Where-Object { ($_.DisplayName -like $orgMatch) })
            }
            Write-Output ("Provisioned PowerApps environment with name: '" + $environment.DisplayName + "'")
        }

        Write-Output 'Waiting for CDS organization provisioning. This may take several minutes.'
        if (-not $credential) {
            $sleep = 120
            Write-Output 'You may be prompted for credentials multiple times while checking the status of the provisioning.'
        }

        while ($null -eq $crmOrg) {
            Start-Sleep -Seconds $sleep
            $crmOrg = (Get-CrmOrganizations @getCrmOrgParams) | Where-Object { $_.FriendlyName -eq $orgFriendlyName }
        }
    }
    else {
        $crmOrgs = Get-CrmOrganizations @getCrmOrgParams
        if ($UseDefaultOrganization -eq $true) {
            $crmOrg = $crmOrgs | Where-Object { $_.FriendlyName -match $orgMatch }
        }
        else {
            $crmOrg = $crmOrgs | Where-Object { $_.FriendlyName -eq $orgFriendlyName }
        }
    }

    Write-Output '================================================================================='
    Write-Output 'Values for PowerAI LCS Add-In:'
    Write-Output ("  CDS organization url:             " + $crmOrg.WebApplicationUrl)
    Write-Output ("  CDS organization ID:              " + $crmOrg.OrganizationId)
}
catch {
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $_.Exception.InnerException
    while ($null -ne $inner) {
        Write-Output 'Inner Exception:'
        Write-Error $_.Exception.Message
        Write-Warning $_.Exception.StackTrace
        $inner = $inner.InnerException
    }
}
```
---

## <a name="configure-the-azure-setup"></a><span data-ttu-id="f90b3-148">De Azure-instellingen configureren</span><span class="sxs-lookup"><span data-stu-id="f90b3-148">Configure the Azure setup</span></span>

### <a name="enter-the-dataverse-directory-id-and-the-users-azure-ad-object-id"></a><span data-ttu-id="f90b3-149">De Dataverse-directory-id en de Azure AD-object-id van de gebruiker invoeren</span><span class="sxs-lookup"><span data-stu-id="f90b3-149">Enter the Dataverse directory ID and the user's Azure AD object ID</span></span>

1. <span data-ttu-id="f90b3-150">Voer de Dataverse-directory-id in:</span><span class="sxs-lookup"><span data-stu-id="f90b3-150">Enter the Dataverse directory ID:</span></span>

    1. <span data-ttu-id="f90b3-151">Open de [Azure Portal](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="f90b3-151">Open the [Azure portal](https://portal.azure.com).</span></span>
    2. <span data-ttu-id="f90b3-152">Meld u aan met de gebruikers-id die is gebruikt om de Dataverse-omgeving te maken.</span><span class="sxs-lookup"><span data-stu-id="f90b3-152">Sign in by using the user ID that was used to create the Dataverse environment.</span></span>
    3. <span data-ttu-id="f90b3-153">Ga naar **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-153">Go to **Azure Active Directory**.</span></span>
    4. <span data-ttu-id="f90b3-154">Kopieer de waarde van de **Tenant-id**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-154">Copy the **Tenant ID** value.</span></span>

2. <span data-ttu-id="f90b3-155">Voer de Azure Active Directory (Azure AD) object-id van de gebruiker in:</span><span class="sxs-lookup"><span data-stu-id="f90b3-155">Enter the user's Azure Active Directory (Azure AD) object ID:</span></span>

    1. <span data-ttu-id="f90b3-156">Ga in de [Azure-portal](https://portal.azure.com) naar **Gebruikers** en zoek de gebruiker op basis van het e-mailadres.</span><span class="sxs-lookup"><span data-stu-id="f90b3-156">In the [Azure portal](https://portal.azure.com), go to **Users**, and search for the user by email address.</span></span>
    2. <span data-ttu-id="f90b3-157">Selecteer de naam van de gebruiker.</span><span class="sxs-lookup"><span data-stu-id="f90b3-157">Select the user's name.</span></span>
    3. <span data-ttu-id="f90b3-158">Kopieer de waarde van de **Object-id**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-158">Copy the **Object ID** value.</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="f90b3-159">De Azure Cloud Shell gebruiken om Data Lake-resources voor Financiële inzichten in te stellen</span><span class="sxs-lookup"><span data-stu-id="f90b3-159">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="f90b3-160">Windows PowerShell-script gebruiken</span><span class="sxs-lookup"><span data-stu-id="f90b3-160">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="f90b3-161">Er is een Windows PowerShell-script meegeleverd, zodat u eenvoudig de Azure-resources kunt instellen die worden beschreven in de module [Export naar Azure Data Lake configureren](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/configure-export-data-lake).</span><span class="sxs-lookup"><span data-stu-id="f90b3-161">A Windows PowerShell script has been provided, so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/configure-export-data-lake).</span></span> <span data-ttu-id="f90b3-162">Als u liever handmatig de instellingen opgeeft, slaat u deze procedure over en gaat u verder met de procedure in de sectie [Handmatige instellingen](#manual-setup).</span><span class="sxs-lookup"><span data-stu-id="f90b3-162">If you prefer to do manual setup, skip this procedure, and continue with the procedure in the [Manual setup](#manual-setup) section.</span></span>

> [!NOTE]
> <span data-ttu-id="f90b3-163">Voer de volgende stappen uit om het PowerShell-script uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="f90b3-163">Follow the steps below to run the PowerShell script.</span></span> <span data-ttu-id="f90b3-164">De Azure CLI-optie 'Probeer het' of het uitvoeren van het script op uw pc werkt mogelijk niet.</span><span class="sxs-lookup"><span data-stu-id="f90b3-164">The Azure CLI "Try it" option, or running the script on your PC may not work.</span></span>

<span data-ttu-id="f90b3-165">Voer de volgende stappen uit om Azure te configureren met het Windows PowerShell-script.</span><span class="sxs-lookup"><span data-stu-id="f90b3-165">Follow these steps to configure Azure by using the Windows PowerShell script.</span></span> <span data-ttu-id="f90b3-166">U moet beschikken over rechten om een Azure-resourcegroep, Azure-resources en een Azure AD-toepassing te maken.</span><span class="sxs-lookup"><span data-stu-id="f90b3-166">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="f90b3-167">Zie voor informatie over de vereiste machtigingen [Azure AD-machtigingen controleren](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span><span class="sxs-lookup"><span data-stu-id="f90b3-167">For information about the required permissions, see [Check Azure AD permissions](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="f90b3-168">Ga in de [Azure Portal](https://portal.azure.com) naar het Azure-abonnement van uw bestemming.</span><span class="sxs-lookup"><span data-stu-id="f90b3-168">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span> <span data-ttu-id="f90b3-169">Selecteer de knop **Cloud Shell** rechts van het veld **Zoeken**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-169">Select the **Cloud Shell** button to the right of the **Search** field.</span></span>
2. <span data-ttu-id="f90b3-170">Selecteer **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-170">Select **PowerShell**.</span></span>
3. <span data-ttu-id="f90b3-171">Maak opslagruimte, als u hierom wordt gevraagd.</span><span class="sxs-lookup"><span data-stu-id="f90b3-171">Create storage, if you're prompted to do so.</span></span> <span data-ttu-id="f90b3-172">Upload het Windows PowerShell-script naar de sessie.</span><span class="sxs-lookup"><span data-stu-id="f90b3-172">Then upload the Windows PowerShell script to the session.</span></span>
4. <span data-ttu-id="f90b3-173">Voer het script uit.</span><span class="sxs-lookup"><span data-stu-id="f90b3-173">Run the script.</span></span>
5. <span data-ttu-id="f90b3-174">Volg de aanwijzingen om het script uit te voeren.</span><span class="sxs-lookup"><span data-stu-id="f90b3-174">Follow the prompts to run the script.</span></span>
6. <span data-ttu-id="f90b3-175">Gebruik de informatie uit de scriptuitvoer om de invoegtoepassing **Exporteren naar Data Lake** in LCS te installeren.</span><span class="sxs-lookup"><span data-stu-id="f90b3-175">Use the information from the script output to install the **Export to Data Lake** add-in in LCS.</span></span>
7. <span data-ttu-id="f90b3-176">Gebruik de informatie uit de scriptuitvoer om de entiteitsopslag in te schakelen op de pagina **Gegevensverbindingen** in Financiën (**Systeembeheer \> Systeemparameters \> Gegevensverbindingen**).</span><span class="sxs-lookup"><span data-stu-id="f90b3-176">Use the information from the script output to enable the entity store on the **Data connections** page in Finance (**System administration \> System parameters \> Data connections**).</span></span>

### <a name="manual-setup"></a><span data-ttu-id="f90b3-177">Handmatige installatie</span><span class="sxs-lookup"><span data-stu-id="f90b3-177">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="f90b3-178">Toepassingen toevoegen aan de Azure AD-tenant</span><span class="sxs-lookup"><span data-stu-id="f90b3-178">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="f90b3-179">Ga in de [Azure Portal](https://portal.azure.com) naar **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-179">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="f90b3-180">Selecteer **Beheren \> Ondernemingstoepassingen**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-180">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="f90b3-181">Zoek naar de volgende toepassingen op app-id.</span><span class="sxs-lookup"><span data-stu-id="f90b3-181">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="f90b3-182">Sollicitatie</span><span class="sxs-lookup"><span data-stu-id="f90b3-182">Application</span></span>                              | <span data-ttu-id="f90b3-183">App-id</span><span class="sxs-lookup"><span data-stu-id="f90b3-183">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="f90b3-184">Microsoft Dynamics ERP-microservices</span><span class="sxs-lookup"><span data-stu-id="f90b3-184">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="f90b3-185">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="f90b3-185">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="f90b3-186">Microsoft Dynamics ERP-microservices CDS</span><span class="sxs-lookup"><span data-stu-id="f90b3-186">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="f90b3-187">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="f90b3-187">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="f90b3-188">AI Builder-autorisatieservice</span><span class="sxs-lookup"><span data-stu-id="f90b3-188">AI Builder Authorization Service</span></span>         | <span data-ttu-id="f90b3-189">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="f90b3-189">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="f90b3-190">Als u geen van de voorgaande toepassingen kunt vinden, voert u de volgende stappen uit.</span><span class="sxs-lookup"><span data-stu-id="f90b3-190">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="f90b3-191">Selecteer op uw lokale computer het menu **Start** en zoek naar **powershell**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-191">On your local machine, select the **Start** menu, and search for **powershell**.</span></span>
2. <span data-ttu-id="f90b3-192">Selecteer **Windows PowerShell** en houd ingedrukt (of klik met de rechtermuisknop) en selecteer **Uitvoeren als beheerder**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-192">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="f90b3-193">Voer de volgende opdracht uit om de **AzureAD**-module te installeren.</span><span class="sxs-lookup"><span data-stu-id="f90b3-193">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="f90b3-194">Als een NuGet-provider vereist is om door te gaan, selecteert u **J** om deze te installeren.</span><span class="sxs-lookup"><span data-stu-id="f90b3-194">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="f90b3-195">Als het bericht 'Niet-vertrouwde opslagplaats' wordt weergegeven, selecteert u **J** om door te gaan.</span><span class="sxs-lookup"><span data-stu-id="f90b3-195">If an "Untrusted repository" message appears, select **Y** to continue.</span></span>
6. <span data-ttu-id="f90b3-196">Voer voor elke toepassing die moet worden toegevoegd de volgende opdrachten uit om de toepassing toe te voegen aan Azure AD.</span><span class="sxs-lookup"><span data-stu-id="f90b3-196">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="f90b3-197">Meld u aan als Azure AD-beheerder als dat wordt gevraagd.</span><span class="sxs-lookup"><span data-stu-id="f90b3-197">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="f90b3-198">Azure-resources maken</span><span class="sxs-lookup"><span data-stu-id="f90b3-198">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="f90b3-199">Zorg ervoor dat u de volgende resources in hetzelfde Azure AD-exemplaar maakt als de Dataverse-omgeving.</span><span class="sxs-lookup"><span data-stu-id="f90b3-199">Make sure that you create the following resources in the same Azure AD instance as the Dataverse environment.</span></span> <span data-ttu-id="f90b3-200">U kunt resources uit een ander Azure AD-exemplaar niet gebruiken.</span><span class="sxs-lookup"><span data-stu-id="f90b3-200">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="f90b3-201">Een nieuw opslagaccount maken:</span><span class="sxs-lookup"><span data-stu-id="f90b3-201">Create a new storage account:</span></span>

    1. <span data-ttu-id="f90b3-202">Maak een opslag account in de [Azure Portal](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="f90b3-202">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="f90b3-203">Stel in het dialoogvenster **Opslagaccount maken** de volgende velden in:</span><span class="sxs-lookup"><span data-stu-id="f90b3-203">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="f90b3-204">**Locatie**: selecteer het datacentrum waar uw omgeving zich bevindt.</span><span class="sxs-lookup"><span data-stu-id="f90b3-204">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="f90b3-205">**Prestaties**: we raden u aan om **Standaard** te selecteren.</span><span class="sxs-lookup"><span data-stu-id="f90b3-205">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="f90b3-206">**Soort account**: selecteer **StorageV2**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-206">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="f90b3-207">Selecteer **Inschakelen** onder **Hiërarchische naamruimten** in het dialoogvenster **Geavanceerde opties** voor de optie **Data Lake Storage Gen2**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-207">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="f90b3-208">Als u deze functie uitschakelt, kunt u geen gegevens gebruiken die door Finance and Operations-apps worden geschreven met behulp van services zoals Power BI-gegevensstromen.</span><span class="sxs-lookup"><span data-stu-id="f90b3-208">If you disable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="f90b3-209">Selecteer **Controleren en maken**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-209">Select **Review and create**.</span></span> <span data-ttu-id="f90b3-210">Wanneer de implementatie is voltooid, wordt de nieuwe resource weergegeven in de Azure Portal.</span><span class="sxs-lookup"><span data-stu-id="f90b3-210">When the deployment is completed, the new resource will be shown in the Azure portal.</span></span>
    5. <span data-ttu-id="f90b3-211">Ga naar het opslagaccount dat u hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="f90b3-211">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="f90b3-212">Selecteer **Toegangssleutels** in het linkermenu.</span><span class="sxs-lookup"><span data-stu-id="f90b3-212">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="f90b3-213">Kopieer de verbindingstekenreeks en sla deze op voor **Key1** of **Key2**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-213">Copy and save the connection string for either **Key1** or **Key2**.</span></span>
    8. <span data-ttu-id="f90b3-214">Kopieer de naam van het opslagaccount en sla deze op.</span><span class="sxs-lookup"><span data-stu-id="f90b3-214">Copy and save the storage account name.</span></span>

2. <span data-ttu-id="f90b3-215">Een Key Vault maken:</span><span class="sxs-lookup"><span data-stu-id="f90b3-215">Create a new key vault:</span></span>

    1. <span data-ttu-id="f90b3-216">Maak een Key Vault in de [Azure Portal](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="f90b3-216">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="f90b3-217">Selecteer in het dialoogvenster **Key Vault maken** in het veld **Locatie** het datacentrum waar uw omgeving zich bevindt.</span><span class="sxs-lookup"><span data-stu-id="f90b3-217">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="f90b3-218">Nadat de Key Vault is gemaakt, selecteert u deze in de lijst en selecteert u **Geheimen**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-218">After key vault is created, select it in the list, and then select **Secrets**.</span></span>
    4. <span data-ttu-id="f90b3-219">Selecteer **Genereren/Importeren**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-219">Select **Generate/Import**.</span></span>
    5. <span data-ttu-id="f90b3-220">Selecteer in het dialoogvenster **Een geheim maken** in het veld **Opties voor uploaden** de optie **Handmatig**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-220">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
    6. <span data-ttu-id="f90b3-221">Voer een naam voor het geheim in.</span><span class="sxs-lookup"><span data-stu-id="f90b3-221">Enter a name for the secret.</span></span> <span data-ttu-id="f90b3-222">Noteer de naam, omdat u deze later moet opgeven.</span><span class="sxs-lookup"><span data-stu-id="f90b3-222">Make a note of the name, because you will have to provide it later.</span></span>
    7. <span data-ttu-id="f90b3-223">Voer in het veld **Waarde** de verbindingsreeks in die u hebt verkregen uit het opslagaccount in de vorige procedure.</span><span class="sxs-lookup"><span data-stu-id="f90b3-223">In the **Value** field, enter the connection string that you obtained from the storage account in the previous procedure.</span></span>
    8. <span data-ttu-id="f90b3-224">Selecteer **Ingeschakeld** en vervolgens **Maken**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-224">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="f90b3-225">Het geheim wordt gemaakt en toegevoegd aan Key Vault.</span><span class="sxs-lookup"><span data-stu-id="f90b3-225">The secret is created and added to Key Vault.</span></span>
    9. <span data-ttu-id="f90b3-226">Ga naar **Overzicht van Key Vault** en noteer de DNS-naam.</span><span class="sxs-lookup"><span data-stu-id="f90b3-226">Go to the **Key Vault Overview**, and make a note of the DNS name.</span></span>

3. <span data-ttu-id="f90b3-227">Een Azure AD-toepassing maken en registreren:</span><span class="sxs-lookup"><span data-stu-id="f90b3-227">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="f90b3-228">Ga in de [Azure Portal](https://portal.azure.com) naar **Azure Active Directory** en selecteer **App-registraties**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-228">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="f90b3-229">Selecteer **Nieuwe toepassingsregistratie** en stel de volgende velden in:</span><span class="sxs-lookup"><span data-stu-id="f90b3-229">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="f90b3-230">**Naam**: voer de naam van de app in.</span><span class="sxs-lookup"><span data-stu-id="f90b3-230">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="f90b3-231">**Toepassingstype**: selecteer **Web-API**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-231">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="f90b3-232">**Omleidings-URL instellen**: voer de URL in voor uw Dynamics 365-exemplaar, bijvoorbeeld,`https://yourdynamicsinstance.dynamics.com/auth`.</span><span class="sxs-lookup"><span data-stu-id="f90b3-232">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as, `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="f90b3-233">Ga naar de app die u zojuist hebt gemaakt om de waarde van de **Toepassings-id (client)** te kopiëren en op te slaan.</span><span class="sxs-lookup"><span data-stu-id="f90b3-233">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="f90b3-234">Wanneer u de Key Vault instelt, moet u deze waarde later opgeven.</span><span class="sxs-lookup"><span data-stu-id="f90b3-234">You will have to provide this value later, when you set up the key vault.</span></span>
    4. <span data-ttu-id="f90b3-235">Ga naar **API-machtigingen** en voer de volgende stappen uit:</span><span class="sxs-lookup"><span data-stu-id="f90b3-235">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="f90b3-236">Selecteer **Een machtiging toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-236">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="f90b3-237">Selecteer **Azure Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-237">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="f90b3-238">Nadat u gedelegeerde machtigingen hebt geselecteerd, selecteert u **gebruikers\_imitatie**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-238">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="f90b3-239">Selecteer **Machtigingen toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-239">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="f90b3-240">Selecteer in het menu voor de app **Certificaten \& geheimen** en voer de volgende stappen uit om Key Vault-geheimen te maken:</span><span class="sxs-lookup"><span data-stu-id="f90b3-240">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="f90b3-241">Selecteer **Nieuw clientgeheim**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-241">Select **New client secret**.</span></span>
        2. <span data-ttu-id="f90b3-242">Voer in het veld **Sleutelbeschrijving** een naam in.</span><span class="sxs-lookup"><span data-stu-id="f90b3-242">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="f90b3-243">Selecteer een duur en vervolgens **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-243">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="f90b3-244">Er wordt een geheim gegenereerd in het veld **Waarde**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-244">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="f90b3-245">Kopieer de geheime waarde en sla deze op.</span><span class="sxs-lookup"><span data-stu-id="f90b3-245">Copy and save the secret value.</span></span>

4. <span data-ttu-id="f90b3-246">Key Vault-geheimen maken:</span><span class="sxs-lookup"><span data-stu-id="f90b3-246">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="f90b3-247">Ga naar de Key Vault die u eerder hebt gemaakt en selecteer **Geheimen**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-247">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="f90b3-248">Voer de volgende stappen uit voor elke geheime naam in de onderstaande tabel:</span><span class="sxs-lookup"><span data-stu-id="f90b3-248">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="f90b3-249">Selecteer **Genereren/Importeren**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-249">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="f90b3-250">Selecteer in het dialoogvenster **Een geheim maken** in het veld **Opties voor uploaden** de optie **Handmatig**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-250">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="f90b3-251">Maak de geheime naam en waarde uit de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="f90b3-251">Create the secret name and value from the following table.</span></span>
        4. <span data-ttu-id="f90b3-252">Selecteer **Ingeschakeld** en vervolgens **Maken**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-252">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="f90b3-253">Het geheim wordt gemaakt en toegevoegd aan Key Vault.</span><span class="sxs-lookup"><span data-stu-id="f90b3-253">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="f90b3-254">Geheime naam</span><span class="sxs-lookup"><span data-stu-id="f90b3-254">Secret name</span></span>                       | <span data-ttu-id="f90b3-255">Geheime waarde</span><span class="sxs-lookup"><span data-stu-id="f90b3-255">Secret value</span></span>                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | <span data-ttu-id="f90b3-256">app-id</span><span class="sxs-lookup"><span data-stu-id="f90b3-256">app-id</span></span>                            | <span data-ttu-id="f90b3-257">De app-id van de toepassing die u eerder hebt gemaakt</span><span class="sxs-lookup"><span data-stu-id="f90b3-257">The app ID of the application that you created earlier</span></span>                                      |
        | <span data-ttu-id="f90b3-258">app-secret</span><span class="sxs-lookup"><span data-stu-id="f90b3-258">app-secret</span></span>                        | <span data-ttu-id="f90b3-259">Het clientgeheim dat u eerder hebt opgeslagen</span><span class="sxs-lookup"><span data-stu-id="f90b3-259">The client secret that you saved earlier</span></span>                                                    |
        | <span data-ttu-id="f90b3-260">storage-account-name</span><span class="sxs-lookup"><span data-stu-id="f90b3-260">storage-account-name</span></span>              | <span data-ttu-id="f90b3-261">De naam van het opslagaccount dat u eerder hebt gemaakt, zoals **storageaccount1**</span><span class="sxs-lookup"><span data-stu-id="f90b3-261">The name of the storage account that you created earlier, such as **storageaccount1**</span></span>       |
        | <span data-ttu-id="f90b3-262">storage-account-connection-string</span><span class="sxs-lookup"><span data-stu-id="f90b3-262">storage-account-connection-string</span></span> | <span data-ttu-id="f90b3-263">De verbindingsreeks die u van de pagina **Toegangssleutels** voor het opslagaccount hebt gekopieerd</span><span class="sxs-lookup"><span data-stu-id="f90b3-263">The connection string that you copied from the **Access keys** page for the storage account</span></span> |

5. <span data-ttu-id="f90b3-264">De toepassing machtigen om toegang te krijgen tot de Key Vault:</span><span class="sxs-lookup"><span data-stu-id="f90b3-264">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="f90b3-265">Open in de [Azure Portal](https://portal.azure.com) de Key Vault die u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="f90b3-265">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="f90b3-266">Selecteer het toegangsbeleid.</span><span class="sxs-lookup"><span data-stu-id="f90b3-266">Select the access policies.</span></span>
    3. <span data-ttu-id="f90b3-267">Voer de volgende stappen uit voor elke toepassing in de onderstaande tabel:</span><span class="sxs-lookup"><span data-stu-id="f90b3-267">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="f90b3-268">Selecteer **Toegangsbeleid toevoegen** om een toegangsbeleid te maken.</span><span class="sxs-lookup"><span data-stu-id="f90b3-268">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="f90b3-269">Selecteer in het veld **Geheime machtigingen** de machtigingen uit de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="f90b3-269">In the **Secret permissions** field, select the permissions from the following table.</span></span>
        3. <span data-ttu-id="f90b3-270">Zoek in het veld **Principal selecteren** de weergavenaam van de toepassing uit de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="f90b3-270">In the **Select principal** field, search for the application display name from the following table.</span></span>
        4. <span data-ttu-id="f90b3-271">Selecteer **Selecteren**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-271">Select **Select**.</span></span>
        5. <span data-ttu-id="f90b3-272">Selecteer **Toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-272">Select **Add**.</span></span>
        6. <span data-ttu-id="f90b3-273">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-273">Select **Save**.</span></span>

        | <span data-ttu-id="f90b3-274">Sollicitatie</span><span class="sxs-lookup"><span data-stu-id="f90b3-274">Application</span></span>                                              | <span data-ttu-id="f90b3-275">Machtigingen</span><span class="sxs-lookup"><span data-stu-id="f90b3-275">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="f90b3-276">De weergavenaam van de nieuwe toepassing die u hebt gemaakt</span><span class="sxs-lookup"><span data-stu-id="f90b3-276">The display name of the new application that you created</span></span> | <span data-ttu-id="f90b3-277">Ophalen, Lijst</span><span class="sxs-lookup"><span data-stu-id="f90b3-277">Get, List</span></span>   |
        | <span data-ttu-id="f90b3-278">**Microsoft Dynamics ERP-microservices**</span><span class="sxs-lookup"><span data-stu-id="f90b3-278">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="f90b3-279">Ophalen, Lijst</span><span class="sxs-lookup"><span data-stu-id="f90b3-279">Get, List</span></span>   |

6. <span data-ttu-id="f90b3-280">Rollen toewijzen voor toegang tot het opslagaccount:</span><span class="sxs-lookup"><span data-stu-id="f90b3-280">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="f90b3-281">Open in de [Azure Portal](https://portal.azure.com) het opslagaccount dat u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="f90b3-281">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="f90b3-282">Selecteer **Access Control (IAM)** en vervolgens **Roltoewijzingen**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-282">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="f90b3-283">Selecteer **Toevoegen, Roltoewijzing toevoegen**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-283">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="f90b3-284">Voer de volgende stappen uit voor elke toepassing in de onderstaande tabel:</span><span class="sxs-lookup"><span data-stu-id="f90b3-284">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="f90b3-285">Selecteer de rol in de volgende tabel.</span><span class="sxs-lookup"><span data-stu-id="f90b3-285">Select the role from the following table.</span></span>
        2. <span data-ttu-id="f90b3-286">Laat het veld **Toegang toewijzen aan** ingesteld staan op **Azure AD-gebruiker, -groep of serviceprincipal**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-286">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="f90b3-287">Voer in het veld **Selecteren** de toepassing uit de volgende tabel in.</span><span class="sxs-lookup"><span data-stu-id="f90b3-287">In the **Select** field, enter the application from the following table.</span></span>
        4. <span data-ttu-id="f90b3-288">Selecteer **Opslaan**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-288">Select **Save**.</span></span>

        | <span data-ttu-id="f90b3-289">Sollicitatie</span><span class="sxs-lookup"><span data-stu-id="f90b3-289">Application</span></span>                                              | <span data-ttu-id="f90b3-290">Rol</span><span class="sxs-lookup"><span data-stu-id="f90b3-290">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="f90b3-291">De weergavenaam van de nieuwe toepassing die u hebt gemaakt</span><span class="sxs-lookup"><span data-stu-id="f90b3-291">The display name of the new application that you created</span></span> | <span data-ttu-id="f90b3-292">Eigenaar</span><span class="sxs-lookup"><span data-stu-id="f90b3-292">Owner</span></span>                       |
        | <span data-ttu-id="f90b3-293">De weergavenaam van de nieuwe toepassing die u hebt gemaakt</span><span class="sxs-lookup"><span data-stu-id="f90b3-293">The display name of the new application that you created</span></span> | <span data-ttu-id="f90b3-294">Inzender</span><span class="sxs-lookup"><span data-stu-id="f90b3-294">Contributor</span></span>                 |
        | <span data-ttu-id="f90b3-295">De weergavenaam van de nieuwe toepassing die u hebt gemaakt</span><span class="sxs-lookup"><span data-stu-id="f90b3-295">The display name of the new application that you created</span></span> | <span data-ttu-id="f90b3-296">Inzender voor opslagaccounts</span><span class="sxs-lookup"><span data-stu-id="f90b3-296">Storage Account Contributor</span></span> |
        | <span data-ttu-id="f90b3-297">De weergavenaam van de nieuwe toepassing die u hebt gemaakt</span><span class="sxs-lookup"><span data-stu-id="f90b3-297">The display name of the new application that you created</span></span> | <span data-ttu-id="f90b3-298">Eigenaar van gegevens in opslagblob</span><span class="sxs-lookup"><span data-stu-id="f90b3-298">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="f90b3-299">**AI Builder-autorisatieservice**</span><span class="sxs-lookup"><span data-stu-id="f90b3-299">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="f90b3-300">Lezer van gegevens in opslagblob</span><span class="sxs-lookup"><span data-stu-id="f90b3-300">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="f90b3-301">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="f90b3-301">Azure CLI</span></span>](#tab/azure-azure-cli)

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

## <a name="configure-the-entity-store"></a><span data-ttu-id="f90b3-302">De entiteitsopslag configureren</span><span class="sxs-lookup"><span data-stu-id="f90b3-302">Configure the entity store</span></span>

<span data-ttu-id="f90b3-303">Voer de volgende stappen uit om de entiteitsopslag in te stellen in uw Finance-omgeving.</span><span class="sxs-lookup"><span data-stu-id="f90b3-303">Follow these steps to set up the entity store in your Finance environment.</span></span>

1. <span data-ttu-id="f90b3-304">Ga naar **Systeembeheer \> Instellen \> Systeemparameters \> Gegevensverbindingen**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-304">Go to **System administration \> Setup \> System parameters \> Data connections**.</span></span>
2. <span data-ttu-id="f90b3-305">Stel de optie **Data Lake-integratie inschakelen** in op **Ja**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-305">Set the **Enable Data Lake integration** option to **Yes**.</span></span>
3. <span data-ttu-id="f90b3-306">Stel de volgende Key Vault-velden in:</span><span class="sxs-lookup"><span data-stu-id="f90b3-306">Set the following Key Vault fields:</span></span>

    - <span data-ttu-id="f90b3-307">**Toepassings-id (client)**: voer de id van de toepassingsclient in die u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="f90b3-307">**Application (client) ID** – Enter the application client ID that you created earlier.</span></span>
    - <span data-ttu-id="f90b3-308">**Toepassingsgeheim**: voer het geheim in dat u hebt opgeslagen voor de toepassing die u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="f90b3-308">**Application Secret** – Enter the secret that you saved for the application that you created earlier.</span></span>
    - <span data-ttu-id="f90b3-309">**DNS-naam**: u kunt de DNS-naam (Domain Name System) vinden op de pagina met toepassingsdetails voor de toepassing die u eerder hebt gemaakt.</span><span class="sxs-lookup"><span data-stu-id="f90b3-309">**DNS name** – You can find the Domain Name System (DNS) name on the application details page for the application that you created earlier.</span></span>
    - <span data-ttu-id="f90b3-310">**Geheime naam**: voer een **storage-account-connection-string** in.</span><span class="sxs-lookup"><span data-stu-id="f90b3-310">**Secret name** – Enter **storage-account-connection-string**.</span></span>

## <a name="configure-the-data-lake"></a><span data-ttu-id="f90b3-311">Het data lake configureren</span><span class="sxs-lookup"><span data-stu-id="f90b3-311">Configure the data lake</span></span>

<span data-ttu-id="f90b3-312">Voer de volgende stappen uit om de Azure Data Lake-invoegtoepassing aan de omgeving toe te voegen met LCS.</span><span class="sxs-lookup"><span data-stu-id="f90b3-312">Follow these steps to use LCS to add the Azure Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="f90b3-313">Meld u aan bij LCS en selecteer vervolgens **Volledige details** onder de naam van de omgeving aan de rechterkant van de pagina.</span><span class="sxs-lookup"><span data-stu-id="f90b3-313">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="f90b3-314">Selecteer in de sectie **Invoegtoepassingen voor omgeving** de optie **Een nieuwe invoegtoepassing installeren**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-314">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="f90b3-315">Selecteer de invoegtoepassing **Exporteren naar Data Lake**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-315">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="f90b3-316">Voer de volgende waarden in.</span><span class="sxs-lookup"><span data-stu-id="f90b3-316">Enter the following values.</span></span>

    | <span data-ttu-id="f90b3-317">Waarde</span><span class="sxs-lookup"><span data-stu-id="f90b3-317">Value</span></span>                                                              | <span data-ttu-id="f90b3-318">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="f90b3-318">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="f90b3-319">De tenant-id van het Azure-abonnement waarin de Key Vault zich bevindt</span><span class="sxs-lookup"><span data-stu-id="f90b3-319">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="f90b3-320">De tenant-id waar het opslagaccount, de apps en de key vaults zich bevinden.</span><span class="sxs-lookup"><span data-stu-id="f90b3-320">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="f90b3-321">Als u deze waarde wilt zoeken, opent u de [Azure Portal](https://portal.azure.com), gaat u naar **Azure Active Directory** en kopieert u de waarde van **Tenant-id**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-321">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="f90b3-322">Geef de DNS-naam op van uw Key Vault</span><span class="sxs-lookup"><span data-stu-id="f90b3-322">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="f90b3-323">De DNS-naam van de Key Vault, zoals `https://customkeyvault.vault.azure.net/`.</span><span class="sxs-lookup"><span data-stu-id="f90b3-323">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> <span data-ttu-id="f90b3-324">(Deze waarde komt overeen met de DNS-naam die in de entiteitsopslag wordt gebruikt.)</span><span class="sxs-lookup"><span data-stu-id="f90b3-324">(This value matches the DNS name that is used in the entity store.)</span></span> |
    | <span data-ttu-id="f90b3-325">Het geheim opgeven dat de naam van het opslagaccount bevat</span><span class="sxs-lookup"><span data-stu-id="f90b3-325">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="f90b3-326">**storage-account-name**</span><span class="sxs-lookup"><span data-stu-id="f90b3-326">**storage-account-name**</span></span> |
    | <span data-ttu-id="f90b3-327">Geheime naam voor de app-ID die moet worden gebruikt voor toegang tot Data Lake</span><span class="sxs-lookup"><span data-stu-id="f90b3-327">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="f90b3-328">**app-id**</span><span class="sxs-lookup"><span data-stu-id="f90b3-328">**app-id**</span></span> |
    | <span data-ttu-id="f90b3-329">Geheime naam om te gebruiken met app-id</span><span class="sxs-lookup"><span data-stu-id="f90b3-329">Secret name to be used with App ID</span></span>                                 | <span data-ttu-id="f90b3-330">**app-secret**</span><span class="sxs-lookup"><span data-stu-id="f90b3-330">**app-secret**</span></span> |

5. <span data-ttu-id="f90b3-331">Ga akkoord met de voorwaarden en selecteer **Installeren**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-331">Agree to the terms, and select **Install**.</span></span>

<span data-ttu-id="f90b3-332">De invoegtoepassing wordt binnen enkele minuten geïnstalleerd.</span><span class="sxs-lookup"><span data-stu-id="f90b3-332">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-ai-builder"></a><span data-ttu-id="f90b3-333">AI Builder configureren</span><span class="sxs-lookup"><span data-stu-id="f90b3-333">Configure AI Builder</span></span>

1. <span data-ttu-id="f90b3-334">Meld u aan bij LCS en open de pagina **Omgevingsdetails**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-334">Sign in to LCS, and open the **Environment details** page.</span></span>
2. <span data-ttu-id="f90b3-335">Schuif naar de sectie **Invoegtoepassingen voor omgeving**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-335">Scroll to the **Environment add-ins** section.</span></span> <span data-ttu-id="f90b3-336">De invoegtoepassingen die al in deze omgeving zijn geïnstalleerd, worden weergegeven.</span><span class="sxs-lookup"><span data-stu-id="f90b3-336">You should see the add-ins that are already installed in this environment.</span></span> <span data-ttu-id="f90b3-337">Als de invoegtoepassing **Exporteren naar Data Lake** daar niet bij staat, configureert u deze invoegtoepassing.</span><span class="sxs-lookup"><span data-stu-id="f90b3-337">If the **Export to Data Lake** add-in isn't among them, configure this add-in.</span></span>
3. <span data-ttu-id="f90b3-338">Selecteer de invoegtoepassing **Inzichten downloaden**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-338">Select the **Get insights** add-in.</span></span>
4. <span data-ttu-id="f90b3-339">Voer de volgende waarden in op de detailspagina van de invoegtoepassing **Inzichten downloaden**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-339">On the **Get insights** add-in details page, enter the following values.</span></span>

    | <span data-ttu-id="f90b3-340">Waarde</span><span class="sxs-lookup"><span data-stu-id="f90b3-340">Value</span></span>                                                    | <span data-ttu-id="f90b3-341">Beschrijving</span><span class="sxs-lookup"><span data-stu-id="f90b3-341">Description</span></span> |
    |----------------------------------------------------------|-------------|
    | <span data-ttu-id="f90b3-342">Organisatie-URL CDS</span><span class="sxs-lookup"><span data-stu-id="f90b3-342">CDS Organization URL</span></span>                                     | <span data-ttu-id="f90b3-343">De URL van de Dataverse-organisatie van het Dataverse-exemplaar.</span><span class="sxs-lookup"><span data-stu-id="f90b3-343">The Dataverse organization URL of the Dataverse instance.</span></span> <span data-ttu-id="f90b3-344">Om deze waarde te vinden opent u de [Power Apps-portal](https://make.powerapps.com), selecteert u de knop **Instellingen** (tandwielsymbool) in de rechterbovenhoek en **Geavanceerde instellingen**, kopieert u de URL.</span><span class="sxs-lookup"><span data-stu-id="f90b3-344">To find this value, open the [Power Apps portal](https://make.powerapps.com), select the **Settings** button (gear symbol) in the upper-right upper corner, select **Advanced settings**, and copy the URL.</span></span> <span data-ttu-id="f90b3-345">(De URL eindigt op dynamics.com.)</span><span class="sxs-lookup"><span data-stu-id="f90b3-345">(The URL ends with "dynamics.com.")</span></span> |
    | <span data-ttu-id="f90b3-346">CDS Org-id</span><span class="sxs-lookup"><span data-stu-id="f90b3-346">CDS Org ID</span></span>                                               | <span data-ttu-id="f90b3-347">De omgevings-id van het Dataverse-exemplaar.</span><span class="sxs-lookup"><span data-stu-id="f90b3-347">The environment ID of the Dataverse instance.</span></span> <span data-ttu-id="f90b3-348">Om deze waarde te vinden opent u de [Power Apps-portal](https://make.powerapps.com), selecteert u de knop **Instellingen** (tandwielsymbool) in de rechterbovenhoek, selecteert u **Aanpassingen \> Ontwikkelaarresources \> Verwijzingsgegevens van exemplaar** en kopieert u de waarde **Id**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-348">To find this value, open the [Power Apps portal](https://make.powerapps.com), select the **Settings** button (gear symbol) in the upper-right upper corner, select **Customizations \> Developer resources \> Instance Reference Information**, and copy the **ID** value.</span></span> |
    | <span data-ttu-id="f90b3-349">CDS-tenant-id (directory-id van AAD)</span><span class="sxs-lookup"><span data-stu-id="f90b3-349">CDS Tenant ID (Directory ID from AAD)</span></span>               | <span data-ttu-id="f90b3-350">De tenant-id van het Dataverse-exemplaar.</span><span class="sxs-lookup"><span data-stu-id="f90b3-350">The tenant ID of the Dataverse instance.</span></span> <span data-ttu-id="f90b3-351">Als u deze waarde wilt zoeken, opent u de [Azure Portal](https://portal.azure.com), gaat u naar **Azure Active Directory** en kopieert u de waarde van **Tenant-id**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-351">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="f90b3-352">Geef gebruikersobject-id op met systeembeheerderrol</span><span class="sxs-lookup"><span data-stu-id="f90b3-352">Provide user object ID who has system administrator role</span></span> | <span data-ttu-id="f90b3-353">De Azure AD-gebruikersobject-id van de gebruiker in Dataverse.</span><span class="sxs-lookup"><span data-stu-id="f90b3-353">The Azure AD user object ID of the user in Dataverse.</span></span> <span data-ttu-id="f90b3-354">Deze gebruiker moet een systeembeheerder van het Dataverse-exemplaar zijn.</span><span class="sxs-lookup"><span data-stu-id="f90b3-354">This user must be a system administrator of the Dataverse instance.</span></span> <span data-ttu-id="f90b3-355">Als u deze waarde wilt vinden, opent u de [Azure Portal](https://portal.azure.com), gaat u naar **Azure Active Directory \> Gebruikers**, selecteert u de gebruiker en kopieert u vervolgens in de sectie **Identiteit** de waarde **Object-id**.</span><span class="sxs-lookup"><span data-stu-id="f90b3-355">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory \> Users**, select the user, and then, in the **Identity** section, copy the **Object ID** value.</span></span> |
    | <span data-ttu-id="f90b3-356">Is dit de standaard CDS-omgeving voor de tenant?</span><span class="sxs-lookup"><span data-stu-id="f90b3-356">Is this the default CDS environment for the tenant?</span></span>      | <span data-ttu-id="f90b3-357">Schakel dit selectievakje in als het Dataverse-exemplaar het eerste productie-exemplaar is dat is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="f90b3-357">If the Dataverse instance was the first production instance that was created, select this check box.</span></span> <span data-ttu-id="f90b3-358">Als het Dataverse-exemplaar handmatig is gemaakt, schakelt u dit selectievakje uit.</span><span class="sxs-lookup"><span data-stu-id="f90b3-358">If the Dataverse instance was manually created, clear this check box.</span></span> |

## <a name="feedback-and-support"></a><span data-ttu-id="f90b3-359">Feedback en ondersteuning</span><span class="sxs-lookup"><span data-stu-id="f90b3-359">Feedback and support</span></span>

<span data-ttu-id="f90b3-360">Stuur een e-mail naar [Inzichten voor betalingen van klanten (preview)](mailto:fiap@microsoft.com) als u feedback wilt geven of ondersteuning nodig hebt.</span><span class="sxs-lookup"><span data-stu-id="f90b3-360">Please send an email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in providing feedback or need support.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="f90b3-361">Privacyverklaring</span><span class="sxs-lookup"><span data-stu-id="f90b3-361">Privacy notice</span></span>

<span data-ttu-id="f90b3-362">Previews (1) bieden mogelijk minder privacy- en beveiligingsmaatregelen dan de service Dynamics 365 Finance and Operations, (2) worden niet opgenomen in de serviceovereenkomst voor deze service, (3) mogen niet worden gebruikt voor de verwerking van persoonsgegevens of andere gegevens die aan juridische of wettelijke nalevingvereisten zijn onderworpen en (4) worden slechts beperkt ondersteund.</span><span class="sxs-lookup"><span data-stu-id="f90b3-362">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]