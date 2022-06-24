---
title: Configuratie voor Finance Insights - versie 10.0.20 en hoger
description: In dit artikel wordt uitgelegd hoe u uw systeem configureert voor gebruik van de mogelijkheden die beschikbaar zijn in Finance Insights in versie 10.0.20 en hoger.
author: ShivamPandey-msft
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
ROBOTS: noindex,nofollow
audience: Application User
ms.reviewer: kfend
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-06-03
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: e6b9c34ee68a25ac9613a65cf63443751a39c576
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8868513"
---
# <a name="configuration-for-finance-insights---version-10020-and-later"></a>Configuratie voor Finance Insights - versie 10.0.20 en hoger

[!include [banner](../includes/banner.md)]



Finance Insights combineert de functionaliteit van Microsoft Dynamics 365 Finance met Dataverse, Azure en AI Builder, zodat u beschikt over krachtige prognosefuncties voor uw organisatie. In dit artikel wordt uitgelegd hoe u Dynamics 365 Finance versie 10.0.20 configureert zodat uw systeem de mogelijkheden kan gebruiken die beschikbaar zijn in Finance Insights.

> [!NOTE]
> De configuratiestappen die in dit artikel worden beschreven, zijn alleen van toepassing op Finance versie 10.0.20 en hoger. Zie [Configuratie voor Finance Insights - versies tot en met 10.0.19](configure-for-fin-insites.md) als u Finance insights versie 10.0.19 en lager wilt instellen.

## <a name="deploy-finance"></a>Finance implementeren

Ga als volgt te werk om de omgevingen te implementeren.

1. In Microsoft Dynamics Lifecycle Services (LCS) kunt u een Finance-omgeving maken of bijwerken. Voor de omgeving is appversie 10.0.20 of hoger vereist van de apps voor financiële en bedrijfsactiviteiten.
2. De omgeving moet een omgeving met hoge beschikbaarheid (HA) zijn in de sandbox. (Dit type omgeving wordt ook wel een Tier-2-omgeving genoemd.) Zie [Omgevingsplanning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md) voor meer informatie.
3. Als u Finance insights configureert in een Sandbox-omgeving, moet u mogelijk productiegegevens naar die omgeving kopiëren om voorspellingen te kunnen uitvoeren. Het voorspellingsmodel gebruikt meerdere jaren aan gegevens om voorspellingen samen te stellen. De Contoso-demonstratiegegevens bevatten niet voldoende historische gegevens om het voorspellingsmodel op een adequate manier te trainen. 

## <a name="configure-dataverse"></a>Dataverse configureren

Voer de volgende stappen uit om Dataverse voor Finance Insights te configureren.

1. Open de omgevingspagina in LCS en controleer of de sectie **Power Platform-integratie** al is ingesteld.

    - Als deze al is ingesteld, moet de naam van de Dataverse-omgeving worden weergegeven die is gekoppeld aan de Finance-omgeving.
    - Als de sectie niet is ingesteld, voert u deze stappen uit:

        1. Selecteer **Instellingen** in de sectie **Power Platform**-integratie. De instelling van de omgeving kan maximaal een uur duren.
        2. Nadat de Dataverse-omgeving is ingesteld, moet de naam van de Dataverse-omgeving die is gekoppeld aan de Finance-omgeving worden weergegeven.

        > [!NOTE]
        > Nadat u de omgevingsinstellingen hebt voltooid, moet u **Koppeling naar CDS for Apps** **niet** selecteren. Deze knop is niet vereist voor Finance insights. Als u de knop selecteert, kunt u de vereiste omgevingsinvoegtoepassingen in LCS niet configureren.

## <a name="configure-azure"></a>Azure configureren

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a>De Azure Cloud Shell gebruiken om Data Lake-resources voor Finance Insights in te stellen

# <a name="use-a-windows-powershell-script"></a>[Windows PowerShell-script gebruiken](#tab/use-a-powershell-script)

Er is een Windows PowerShell-script meegeleverd, zodat u eenvoudig de Azure-resources kunt instellen die worden beschreven in [Export naar Azure Data Lake configureren](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md). Als u liever handmatig de instellingen opgeeft, slaat u deze procedure over en voltooit u de procedure in de sectie [Handmatige instellingen](#manual-setup) in plaats daarvan.

> [!NOTE]
> Voer de volgende procedure uit om het Windows PowerShell-script uit te voeren. De instellingen werken mogelijk niet als u de optie **Probeer het** gebruikt in Azure CLI of als u het script op uw computer uitvoert.

Voer de volgende stappen uit om Azure te configureren met het Windows PowerShell-script. U moet beschikken over rechten om een Azure-resourcegroep, Azure-resources en een Azure AD-toepassing te maken. Zie voor informatie over de vereiste machtigingen [Azure AD-machtigingen controleren](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).

1. Ga in de [Azure Portal](https://portal.azure.com) naar het Azure-abonnement van uw bestemming.
2. Selecteer **Cloud Shell** rechts van het veld **Zoeken**.
3. Selecteer **PowerShell**.
4. Maak opslagruimte als u dat wordt gevraagd.
5. Selecteer op het tabblad **Azure CLI** de optie **Kopiëren**.
6. Open een nieuw bestand in Kladblok en plak dit in het Windows PowerShell-script.
7. Sla het bestand op met de naam **ConfigureDataLake.ps1**.
8. Upload het Windows PowerShell-script naar de sessie met de menuoptie voor uploaden in Cloud Shell.
9. Voer het script **.\ConfigureDataLake.ps1** uit.
10. Volg de aanwijzingen om het script uit te voeren.
11. Gebruik de informatie uit de scriptuitvoer om de invoegtoepassing Exporteren naar Data Lake in LCS te installeren.

### <a name="manual-setup"></a>Handmatige installatie

#### <a name="add-applications-to-the-azure-ad-tenant"></a>Toepassingen toevoegen aan de Azure AD-tenant

1. Ga in de [Azure Portal](https://portal.azure.com) naar **Azure Active Directory**.
2. Selecteer **Beheren \> Ondernemingstoepassingen**.
3. Zoek naar de volgende toepassingen op app-id.

    | Toepassing                              | App-id                               |
    |------------------------------------------|--------------------------------------|
    | Microsoft Dynamics ERP-microservices     | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |
    | Microsoft Dynamics ERP-microservices CDS | 703e2651-d3fc-48f5-942c-74274233dba8 |
    | AI Builder-autorisatieservice         | ad40333e-9910-4b61-b281-e3aeeb8c3ef3 |

Als u geen van de voorgaande toepassingen kunt vinden, voert u de volgende stappen uit.

1. Selecteer op uw lokale computer het menu **Start** en zoek naar **powershell**.
2. Selecteer **Windows PowerShell** en houd ingedrukt (of klik met de rechtermuisknop) en selecteer **Uitvoeren als beheerder**.
3. Voer de volgende opdracht uit om de **AzureAD**-module te installeren.

    `Install-Module -Name AzureAD`

4. Als een NuGet-provider vereist is om door te gaan, selecteert u **J** om deze te installeren.
5. Als u het bericht 'Niet-vertrouwde opslagplaats' ontvangt, selecteert u **J** om door te gaan.
6. Voer voor elke toepassing die moet worden toegevoegd de volgende opdrachten uit om de toepassing toe te voegen aan Azure AD. Meld u aan als Azure AD-beheerder als dat wordt gevraagd.

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a>Azure-resources maken

> [!NOTE]
> Zorg ervoor dat u de volgende resources in hetzelfde Azure AD-exemplaar maakt als waarin de Dataverse-omgeving zich bevindt. U kunt resources uit een ander Azure AD-exemplaar niet gebruiken.

1. Een nieuw opslagaccount maken:

    1. Maak een opslag account in de [Azure Portal](https://portal.azure.com).
    2. Stel in het dialoogvenster **Opslagaccount maken** de volgende velden in:

        - **Locatie**: selecteer het datacentrum waar uw omgeving zich bevindt.
        - **Prestaties**: we raden u aan om **Standaard** te selecteren.
        - **Soort account**: selecteer **StorageV2**.

    3. Selecteer **Inschakelen** onder **Hiërarchische naamruimten** in het dialoogvenster **Geavanceerde opties** voor de optie **Data Lake Storage Gen2**. Als u deze functie niet inschakelt, kunt u geen gegevens gebruiken die door apps voor financiële en bedrijfsactiviteiten worden geschreven met behulp van services zoals Power BI-gegevensstromen.
    4. Selecteer **Controleren en maken**. Wanneer de implementatie is voltooid, wordt de nieuwe resource weergegeven in de Azure Portal.
    5. Ga naar het opslagaccount dat u hebt gemaakt.
    6. Selecteer **Toegangssleutels** in het linkermenu.
    7. Kopieer de naam van het opslagaccount en sla deze op. Wanneer u de sleutelkluisgeheimen instelt, moet u deze waarde later opgeven.

2. Een sleutelkluis maken:

    1. Maak een Key Vault in de [Azure Portal](https://portal.azure.com).
    2. Selecteer in het dialoogvenster **Key Vault maken** in het veld **Locatie** het datacentrum waar uw omgeving zich bevindt.
    3. Nadat de sleutelkluis is gemaakt, gaat u naar **Overzicht van Key Vault** en kopieert u de DNS-naam en slaat u deze op. Wanneer u de Data Lake-invoegtoepassing instelt, moet u deze waarde later opgeven.

3. Een Azure AD-toepassing maken en registreren:

    1. Ga in de [Azure Portal](https://portal.azure.com) naar **Azure Active Directory** en selecteer **App-registraties**.
    2. Selecteer **Nieuwe toepassingsregistratie** en stel de volgende velden in:

        - **Naam**: voer de naam van de app in.
        - **Toepassingstype**: selecteer **Web-API**.
        - **Omleidings-URL instellen**: voer de URL in voor uw Dynamics 365-exemplaar, bijvoorbeeld `https://yourdynamicsinstance.dynamics.com/auth`.

    3. Ga naar de app die u zojuist hebt gemaakt om de waarde van de **Toepassings-id (client)** te kopiëren en op te slaan. Wanneer u de sleutelkluisgeheimen instelt, moet u deze waarde later opgeven.
    4. Ga naar **API-machtigingen** en voer de volgende stappen uit:

        1. Selecteer **Een machtiging toevoegen**.
        2. Selecteer **Azure Key Vault**.
        3. Nadat u gedelegeerde machtigingen hebt geselecteerd, selecteert u **gebruikers\_imitatie**.
        4. Selecteer **Machtigingen toevoegen**.

    5. Selecteer in het menu voor de app **Certificaten \& geheimen** en voer de volgende stappen uit om Key Vault-geheimen te maken:

        1. Selecteer **Nieuw clientgeheim**.
        2. Voer in het veld **Sleutelbeschrijving** een naam in.
        3. Selecteer een duur en vervolgens **Toevoegen**. Er wordt een geheim gegenereerd in het veld **Waarde**.
        4. Kopieer de clientgeheimwaarde en sla deze op. Wanneer u de sleutelkluisgeheimen instelt, moet u deze waarde later opgeven.

4. Key Vault-geheimen maken:

    1. Ga naar de Key Vault die u eerder hebt gemaakt en selecteer **Geheimen**.
    2. Voer de volgende stappen uit voor elke geheime naam in de onderstaande tabel:

        1. Selecteer **Genereren/Importeren**.
        2. Selecteer in het dialoogvenster **Een geheim maken** in het veld **Opties voor uploaden** de optie **Handmatig**.
        3. Maak de geheime naam en waarde op basis van de volgende tabel.
        4. Selecteer **Ingeschakeld** en vervolgens **Maken**. Het geheim wordt gemaakt en toegevoegd aan Key Vault.

        | Geheime naam                       | Geheime waarde                                                                                 |
        |-----------------------------------|----------------------------------------------------------------------------------------------|
        | app-id                            | De app-id van de toepassing die u eerder hebt gemaakt.                                      |
        | app-secret                        | Het clientgeheim dat u eerder hebt opgeslagen.                                                    |
        | storage-account-name              | De naam van het opslagaccount dat u eerder hebt gemaakt, zoals **storageaccount1**.       |

5. De toepassing machtigen om toegang te krijgen tot de Key Vault:

    1. Open in de [Azure Portal](https://portal.azure.com) de Key Vault die u eerder hebt gemaakt.
    2. Selecteer het toegangsbeleid.
    3. Voer de volgende stappen uit voor elke toepassing in de onderstaande tabel:

        1. Selecteer **Toegangsbeleid toevoegen** om een toegangsbeleid te maken.
        2. Selecteer in het veld **Geheime machtigingen** de machtigingen uit de tabel.
        3. Zoek in het veld **Principal selecteren** de weergavenaam van de toepassing uit de tabel.
        4. Selecteer **Selecteren**.
        5. Selecteer **Toevoegen**.
        6. Selecteer **Opslaan**.

        | Sollicitatie                                              | Machtigingen |
        |----------------------------------------------------------|-------------|
        | De weergavenaam van de nieuwe toepassing die u hebt gemaakt | Ophalen, Lijst   |
        | **Microsoft Dynamics ERP-microservices**                 | Ophalen, Lijst   |

6. Rollen toewijzen voor toegang tot het opslagaccount:

    1. Open in de [Azure Portal](https://portal.azure.com) het opslagaccount dat u eerder hebt gemaakt.
    2. Selecteer **Access Control (IAM)** en vervolgens **Roltoewijzingen**.
    3. Selecteer **Toevoegen, Roltoewijzing toevoegen**.
    4. Voer de volgende stappen uit voor elke toepassing in de onderstaande tabel:

        1. Selecteer de rol in de tabel.
        2. Laat het veld **Toegang toewijzen aan** ingesteld staan op **Azure AD-gebruiker, -groep of serviceprincipal**.
        3. Voer in het veld **Selecteren** de toepassing uit de tabel in.
        4. Selecteer **Opslaan**.

        | Sollicitatie                                              | Rol                        |
        |----------------------------------------------------------|-----------------------------|
        | De weergavenaam van de nieuwe toepassing die u hebt gemaakt | Eigenaar                       |
        | De weergavenaam van de nieuwe toepassing die u hebt gemaakt | Inzender                 |
        | De weergavenaam van de nieuwe toepassing die u hebt gemaakt | Inzender voor opslagaccounts |
        | De weergavenaam van de nieuwe toepassing die u hebt gemaakt | Eigenaar van gegevens in opslagblob     |
        | **AI Builder-autorisatieservice**                     | Lezer van gegevens in opslagblob    |

# <a name="azure-cli"></a>[Azure CLI](#tab/azure-azure-cli)

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

## <a name="configure-the-export-to-data-lake-add-in"></a>Invoegtoepassing Export naar Data Lake configureren

Voer de volgende stappen uit om de invoegtoepassing Export naar Data Lake aan de omgeving toe te voegen met LCS.

1. Meld u aan bij LCS en selecteer vervolgens **Volledige details** onder de naam van de omgeving aan de rechterkant van de pagina.
2. Selecteer in de sectie **Invoegtoepassingen voor omgeving** de optie **Een nieuwe invoegtoepassing installeren**.
3. Selecteer de invoegtoepassing **Exporteren naar Data Lake**.
4. Voer de volgende waarden in.

    | Waarde                                                              | Beschrijving |
    |--------------------------------------------------------------------|-------------|
    | De tenant-id van het Azure-abonnement waarin de Key Vault zich bevindt | De tenant-id waar het opslagaccount, de apps en de key vaults zich bevinden. Als u deze waarde wilt verkrijgen, opent u de [Azure Portal](https://portal.azure.com), gaat u naar **Azure Active Directory** en kopieert u de waarde van **Tenant-id**. |
    | Geef de DNS-naam op van uw Key Vault                             | De DNS-naam van de Key Vault, zoals `https://customkeyvault.vault.azure.net/`. |
    | Het geheim opgeven dat de naam van het opslagaccount bevat   | **storage-account-name** |
    | Geheime naam voor de app-ID die moet worden gebruikt voor toegang tot Data Lake          | **app-id** |
    | Geheime naam voor clientgeheim van app                                  | **app-secret** |

5. Ga akkoord met de voorwaarden en selecteer vervolgens **Installeren**.

De invoegtoepassing wordt binnen enkele minuten geïnstalleerd.

## <a name="configure-the-finance-insights-add-in"></a>De invoegtoepassing Finance insights configureren

> [!NOTE]
> Als u de invoegtoepassing Inzichten ophalen eerder hebt geïnstalleerd, moet u de installatie ongedaan maken voordat u de volgende procedure voltooit.

Voer de volgende stappen uit om de invoegtoepassing Finance insights te installeren.

1. Meld u aan bij LCS en selecteer vervolgens **Volledige details** onder de naam van de omgeving aan de rechterkant van de pagina.
2. Selecteer in de sectie **Invoegtoepassingen voor omgeving** de optie **Een nieuwe invoegtoepassing installeren**.
3. Selecteer de invoegtoepassing **Finance insights**.
4. Ga akkoord met de voorwaarden en selecteer vervolgens **Installeren**.

Het kan enkele minuten duren voordat de invoegtoepassing is geïnstalleerd.

## <a name="feedback-and-support"></a>Feedback en ondersteuning

Stuur een e-mail naar [Finance insights](mailto:fiap@microsoft.com) als u feedback wilt geven of ondersteuning nodig hebt.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
