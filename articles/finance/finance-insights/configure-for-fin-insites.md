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
ms.openlocfilehash: bb887bbff5eb5b92f588d3fa966ea204633575db
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115627"
---
# <a name="configuration-for-finance-insights-preview"></a>Configuratie voor Financiële inzichten (preview)

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Financiële inzichten combineert de functionaliteit van Microsoft Dynamics 365 Finance met Microsoft Dataverse, Azure en AI Builder, zodat u beschikt over krachtige prognosefuncties voor uw organisatie. In dit onderwerp worden de configuratiestappen beschreven die ervoor zorgen dat uw systeem de mogelijkheden gebruikt die beschikbaar zijn in Financiële inzichten.

## <a name="deploy-dynamics-365-finance"></a>Dynamics 365 Finance implementeren

Ga als volgt te werk om de omgevingen te implementeren.

1. In Microsoft Dynamics Lifecycle Services (LCS) kunt u een Dynamics 365 Finance-omgeving maken of bijwerken. Voor de omgeving is app-versie 10.0.11/Platform update 35 of hoger vereist.
2. De omgeving moet een omgeving met hoge beschikbaarheid (HA) zijn in de sandbox. (Dit type omgeving wordt ook wel een Tier-2-omgeving genoemd.) Zie [Omgevingsplanning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md) voor meer informatie.
3. Als u Contoso-demogegevens gebruikt, hebt u aanvullende voorbeeldgegevens nodig om de functies Voorspellingen voor klantbetalingen, Cashflowprognoses en Budgetprognoses te gebruiken. 

## <a name="configure-dataverse"></a>Dataverse configureren

U kunt de volgende handmatige configuratiestappen uitvoeren, of u kunt het configuratieproces versnellen met behulp van het Windows PowerShell-script dat wordt meegeleverd. Na het uitvoeren het PowerShell-script krijgt u waarden die u kunt gebruiken voor het configureren van Financiële inzichten. 

> [!NOTE]
> Open PowerShell op de pc om het script uit te voeren. U hebt mogelijk PowerShell versie 5 nodig. De Microsoft Azure Cli-optie 'Probeer het' werkt mogelijk niet.

# <a name="manual-configuration-steps"></a>[Handmatige configuratiestappen](#tab/configuration-steps)

1. Open het [Power Platform-beheercentrum](https://admin.powerplatform.microsoft.com/) en voer de volgende stappen uit om een nieuwe Dataverse-omgeving te maken in dezelfde Active Directory-tenant:

    1. Open de pagina **Omgevingen**.

        [![Pagina Omgevingen](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)

    2. Selecteer **Nieuwe omgeving**.
    3. Selecteer **Sandbox** in het veld **Type**.
    4. Stel de optie **Database maken** in op **Ja**.
    5. Selecteer **Volgende**.
    6. Selecteer de taal en valuta voor uw organisatie.
    7. Accepteer de standaardwaarden voor de overige velden.
    8. Selecteer **Opslaan**.
    9. Vernieuw de pagina **Omgevingen**.
    10. Wacht totdat de waarde van het veld **Status** is bijgewerkt naar **Gereed**.
    11. Noteer de id van de Dataverse-organisatie.
    12. Selecteer de omgeving en selecteer vervolgens **Instellingen**.
    13. Selecteer **Resources \> Alle oude instellingen**.
    14. Selecteer op de bovenste navigatiebalk **Instellingen** en vervolgens **Aanpassingen**.
    15. Selecteer **Resources voor ontwikkelaars**.
    16. Stel het veld **Id van verwijzingsgegevens van exemplaar** in op de id van de Dataverse-organisatie die u eerder hebt genoteerd.
    17. Noteer de URL voor de Dataverse-organisatie in de adresbalk van de browser. De URL kan bijvoorbeeld `https://org42b2b3d3.crm.dynamics.com` zijn.

2. Als u de functie Cashflowprognoses of Budgetprognoses wilt gebruiken, voert u de volgende stappen uit om de annotatielimiet voor uw organisatie bij te werken tot minimaal 50 MB:

    1. Open de [Power Apps-portal](https://make.powerapps.com).
    2. Selecteer de omgeving die u zojuist hebt gemaakt en selecteer vervolgens **Geavanceerde instellingen**.
    3. Selecteer **Instellingen \> E-mailconfiguratie**.
    4. Wijzig de waarde van het veld **Maximale bestandsgrootte** in **51.200**. (De waarde wordt uitgedrukt in kilobytes \[KB\].)
    5. Selecteer **OK** om uw wijzigingen op te slaan.

# <a name="windows-powershell-configuration-script"></a>[Windows PowerShell-configuratiescript](#tab/powershell-configuration-script)

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

## <a name="configure-the-azure-setup"></a>De Azure-instellingen configureren

### <a name="enter-the-dataverse-directory-id-and-the-users-azure-ad-object-id"></a>De Dataverse-directory-id en de Azure AD-object-id van de gebruiker invoeren

1. Voer de Dataverse-directory-id in:

    1. Open de [Azure Portal](https://portal.azure.com).
    2. Meld u aan met de gebruikers-id die is gebruikt om de Dataverse-omgeving te maken.
    3. Ga naar **Azure Active Directory**.
    4. Kopieer de waarde van de **Tenant-id**.

2. Voer de Azure Active Directory (Azure AD) object-id van de gebruiker in:

    1. Ga in de [Azure-portal](https://portal.azure.com) naar **Gebruikers** en zoek de gebruiker op basis van het e-mailadres.
    2. Selecteer de naam van de gebruiker.
    3. Kopieer de waarde van de **Object-id**.

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a>De Azure Cloud Shell gebruiken om Data Lake-resources voor Financiële inzichten in te stellen

# <a name="use-a-windows-powershell-script"></a>[Windows PowerShell-script gebruiken](#tab/use-a-powershell-script)

Er is een Windows PowerShell-script meegeleverd, zodat u eenvoudig de Azure-resources kunt instellen die worden beschreven in de module [Export naar Azure Data Lake configureren](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/configure-export-data-lake). Als u liever handmatig de instellingen opgeeft, slaat u deze procedure over en gaat u verder met de procedure in de sectie [Handmatige instellingen](#manual-setup).

> [!NOTE]
> Voer de volgende stappen uit om het PowerShell-script uit te voeren. De Azure CLI-optie 'Probeer het' of het uitvoeren van het script op uw pc werkt mogelijk niet.

Voer de volgende stappen uit om Azure te configureren met het Windows PowerShell-script. U moet beschikken over rechten om een Azure-resourcegroep, Azure-resources en een Azure AD-toepassing te maken. Zie voor informatie over de vereiste machtigingen [Azure AD-machtigingen controleren](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).

1. Ga in de [Azure Portal](https://portal.azure.com) naar het Azure-abonnement van uw bestemming. Selecteer de knop **Cloud Shell** rechts van het veld **Zoeken**.
2. Selecteer **PowerShell**.
3. Maak opslagruimte, als u hierom wordt gevraagd. Upload het Windows PowerShell-script naar de sessie.
4. Voer het script uit.
5. Volg de aanwijzingen om het script uit te voeren.
6. Gebruik de informatie uit de scriptuitvoer om de invoegtoepassing **Exporteren naar Data Lake** in LCS te installeren.
7. Gebruik de informatie uit de scriptuitvoer om de entiteitsopslag in te schakelen op de pagina **Gegevensverbindingen** in Financiën (**Systeembeheer \> Systeemparameters \> Gegevensverbindingen**).

### <a name="manual-setup"></a>Handmatige installatie

#### <a name="add-applications-to-the-azure-ad-tenant"></a>Toepassingen toevoegen aan de Azure AD-tenant

1. Ga in de [Azure Portal](https://portal.azure.com) naar **Azure Active Directory**.
2. Selecteer **Beheren \> Ondernemingstoepassingen**.
3. Zoek naar de volgende toepassingen op app-id.

    | Sollicitatie                              | App-id                               |
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
5. Als het bericht 'Niet-vertrouwde opslagplaats' wordt weergegeven, selecteert u **J** om door te gaan.
6. Voer voor elke toepassing die moet worden toegevoegd de volgende opdrachten uit om de toepassing toe te voegen aan Azure AD. Meld u aan als Azure AD-beheerder als dat wordt gevraagd.

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a>Azure-resources maken

> [!NOTE]
> Zorg ervoor dat u de volgende resources in hetzelfde Azure AD-exemplaar maakt als de Dataverse-omgeving. U kunt resources uit een ander Azure AD-exemplaar niet gebruiken.

1. Een nieuw opslagaccount maken:

    1. Maak een opslag account in de [Azure Portal](https://portal.azure.com).
    2. Stel in het dialoogvenster **Opslagaccount maken** de volgende velden in:

        - **Locatie**: selecteer het datacentrum waar uw omgeving zich bevindt.
        - **Prestaties**: we raden u aan om **Standaard** te selecteren.
        - **Soort account**: selecteer **StorageV2**.

    3. Selecteer **Inschakelen** onder **Hiërarchische naamruimten** in het dialoogvenster **Geavanceerde opties** voor de optie **Data Lake Storage Gen2**. Als u deze functie uitschakelt, kunt u geen gegevens gebruiken die door Finance and Operations-apps worden geschreven met behulp van services zoals Power BI-gegevensstromen.
    4. Selecteer **Controleren en maken**. Wanneer de implementatie is voltooid, wordt de nieuwe resource weergegeven in de Azure Portal.
    5. Ga naar het opslagaccount dat u hebt gemaakt.
    6. Selecteer **Toegangssleutels** in het linkermenu.
    7. Kopieer de verbindingstekenreeks en sla deze op voor **Key1** of **Key2**.
    8. Kopieer de naam van het opslagaccount en sla deze op.

2. Een Key Vault maken:

    1. Maak een Key Vault in de [Azure Portal](https://portal.azure.com).
    2. Selecteer in het dialoogvenster **Key Vault maken** in het veld **Locatie** het datacentrum waar uw omgeving zich bevindt.
    3. Nadat de Key Vault is gemaakt, selecteert u deze in de lijst en selecteert u **Geheimen**.
    4. Selecteer **Genereren/Importeren**.
    5. Selecteer in het dialoogvenster **Een geheim maken** in het veld **Opties voor uploaden** de optie **Handmatig**.
    6. Voer een naam voor het geheim in. Noteer de naam, omdat u deze later moet opgeven.
    7. Voer in het veld **Waarde** de verbindingsreeks in die u hebt verkregen uit het opslagaccount in de vorige procedure.
    8. Selecteer **Ingeschakeld** en vervolgens **Maken**. Het geheim wordt gemaakt en toegevoegd aan Key Vault.
    9. Ga naar **Overzicht van Key Vault** en noteer de DNS-naam.

3. Een Azure AD-toepassing maken en registreren:

    1. Ga in de [Azure Portal](https://portal.azure.com) naar **Azure Active Directory** en selecteer **App-registraties**.
    2. Selecteer **Nieuwe toepassingsregistratie** en stel de volgende velden in:

        - **Naam**: voer de naam van de app in.
        - **Toepassingstype**: selecteer **Web-API**.
        - **Omleidings-URL instellen**: voer de URL in voor uw Dynamics 365-exemplaar, bijvoorbeeld,`https://yourdynamicsinstance.dynamics.com/auth`.

    3. Ga naar de app die u zojuist hebt gemaakt om de waarde van de **Toepassings-id (client)** te kopiëren en op te slaan. Wanneer u de Key Vault instelt, moet u deze waarde later opgeven.
    4. Ga naar **API-machtigingen** en voer de volgende stappen uit:

        1. Selecteer **Een machtiging toevoegen**.
        2. Selecteer **Azure Key Vault**.
        3. Nadat u gedelegeerde machtigingen hebt geselecteerd, selecteert u **gebruikers\_imitatie**.
        4. Selecteer **Machtigingen toevoegen**.

    5. Selecteer in het menu voor de app **Certificaten \& geheimen** en voer de volgende stappen uit om Key Vault-geheimen te maken:

        1. Selecteer **Nieuw clientgeheim**.
        2. Voer in het veld **Sleutelbeschrijving** een naam in.
        3. Selecteer een duur en vervolgens **Toevoegen**. Er wordt een geheim gegenereerd in het veld **Waarde**.
        4. Kopieer de geheime waarde en sla deze op.

4. Key Vault-geheimen maken:

    1. Ga naar de Key Vault die u eerder hebt gemaakt en selecteer **Geheimen**.
    2. Voer de volgende stappen uit voor elke geheime naam in de onderstaande tabel:

        1. Selecteer **Genereren/Importeren**.
        2. Selecteer in het dialoogvenster **Een geheim maken** in het veld **Opties voor uploaden** de optie **Handmatig**.
        3. Maak de geheime naam en waarde uit de volgende tabel.
        4. Selecteer **Ingeschakeld** en vervolgens **Maken**. Het geheim wordt gemaakt en toegevoegd aan Key Vault.

        | Geheime naam                       | Geheime waarde                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | app-id                            | De app-id van de toepassing die u eerder hebt gemaakt                                      |
        | app-secret                        | Het clientgeheim dat u eerder hebt opgeslagen                                                    |
        | storage-account-name              | De naam van het opslagaccount dat u eerder hebt gemaakt, zoals **storageaccount1**       |
        | storage-account-connection-string | De verbindingsreeks die u van de pagina **Toegangssleutels** voor het opslagaccount hebt gekopieerd |

5. De toepassing machtigen om toegang te krijgen tot de Key Vault:

    1. Open in de [Azure Portal](https://portal.azure.com) de Key Vault die u eerder hebt gemaakt.
    2. Selecteer het toegangsbeleid.
    3. Voer de volgende stappen uit voor elke toepassing in de onderstaande tabel:

        1. Selecteer **Toegangsbeleid toevoegen** om een toegangsbeleid te maken.
        2. Selecteer in het veld **Geheime machtigingen** de machtigingen uit de volgende tabel.
        3. Zoek in het veld **Principal selecteren** de weergavenaam van de toepassing uit de volgende tabel.
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

        1. Selecteer de rol in de volgende tabel.
        2. Laat het veld **Toegang toewijzen aan** ingesteld staan op **Azure AD-gebruiker, -groep of serviceprincipal**.
        3. Voer in het veld **Selecteren** de toepassing uit de volgende tabel in.
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

## <a name="configure-the-entity-store"></a>De entiteitsopslag configureren

Voer de volgende stappen uit om de entiteitsopslag in te stellen in uw Finance-omgeving.

1. Ga naar **Systeembeheer \> Instellen \> Systeemparameters \> Gegevensverbindingen**.
2. Stel de optie **Data Lake-integratie inschakelen** in op **Ja**.
3. Stel de volgende Key Vault-velden in:

    - **Toepassings-id (client)**: voer de id van de toepassingsclient in die u eerder hebt gemaakt.
    - **Toepassingsgeheim**: voer het geheim in dat u hebt opgeslagen voor de toepassing die u eerder hebt gemaakt.
    - **DNS-naam**: u kunt de DNS-naam (Domain Name System) vinden op de pagina met toepassingsdetails voor de toepassing die u eerder hebt gemaakt.
    - **Geheime naam**: voer een **storage-account-connection-string** in.

## <a name="configure-the-data-lake"></a>Het data lake configureren

Voer de volgende stappen uit om de Azure Data Lake-invoegtoepassing aan de omgeving toe te voegen met LCS.

1. Meld u aan bij LCS en selecteer vervolgens **Volledige details** onder de naam van de omgeving aan de rechterkant van de pagina.
2. Selecteer in de sectie **Invoegtoepassingen voor omgeving** de optie **Een nieuwe invoegtoepassing installeren**.
3. Selecteer de invoegtoepassing **Exporteren naar Data Lake**.
4. Voer de volgende waarden in.

    | Waarde                                                              | Beschrijving |
    |--------------------------------------------------------------------|-------------|
    | De tenant-id van het Azure-abonnement waarin de Key Vault zich bevindt | De tenant-id waar het opslagaccount, de apps en de key vaults zich bevinden. Als u deze waarde wilt zoeken, opent u de [Azure Portal](https://portal.azure.com), gaat u naar **Azure Active Directory** en kopieert u de waarde van **Tenant-id**. |
    | Geef de DNS-naam op van uw Key Vault                             | De DNS-naam van de Key Vault, zoals `https://customkeyvault.vault.azure.net/`. (Deze waarde komt overeen met de DNS-naam die in de entiteitsopslag wordt gebruikt.) |
    | Het geheim opgeven dat de naam van het opslagaccount bevat   | **storage-account-name** |
    | Geheime naam voor de app-ID die moet worden gebruikt voor toegang tot Data Lake          | **app-id** |
    | Geheime naam om te gebruiken met app-id                                 | **app-secret** |

5. Ga akkoord met de voorwaarden en selecteer **Installeren**.

De invoegtoepassing wordt binnen enkele minuten geïnstalleerd.

## <a name="configure-ai-builder"></a>AI Builder configureren

1. Meld u aan bij LCS en open de pagina **Omgevingsdetails**.
2. Schuif naar de sectie **Invoegtoepassingen voor omgeving**. De invoegtoepassingen die al in deze omgeving zijn geïnstalleerd, worden weergegeven. Als de invoegtoepassing **Exporteren naar Data Lake** daar niet bij staat, configureert u deze invoegtoepassing.
3. Selecteer de invoegtoepassing **Inzichten downloaden**.
4. Voer de volgende waarden in op de detailspagina van de invoegtoepassing **Inzichten downloaden**.

    | Waarde                                                    | Beschrijving |
    |----------------------------------------------------------|-------------|
    | Organisatie-URL CDS                                     | De URL van de Dataverse-organisatie van het Dataverse-exemplaar. Om deze waarde te vinden opent u de [Power Apps-portal](https://make.powerapps.com), selecteert u de knop **Instellingen** (tandwielsymbool) in de rechterbovenhoek en **Geavanceerde instellingen**, kopieert u de URL. (De URL eindigt op dynamics.com.) |
    | CDS Org-id                                               | De omgevings-id van het Dataverse-exemplaar. Om deze waarde te vinden opent u de [Power Apps-portal](https://make.powerapps.com), selecteert u de knop **Instellingen** (tandwielsymbool) in de rechterbovenhoek, selecteert u **Aanpassingen \> Ontwikkelaarresources \> Verwijzingsgegevens van exemplaar** en kopieert u de waarde **Id**. |
    | CDS-tenant-id (directory-id van AAD)               | De tenant-id van het Dataverse-exemplaar. Als u deze waarde wilt zoeken, opent u de [Azure Portal](https://portal.azure.com), gaat u naar **Azure Active Directory** en kopieert u de waarde van **Tenant-id**. |
    | Geef gebruikersobject-id op met systeembeheerderrol | De Azure AD-gebruikersobject-id van de gebruiker in Dataverse. Deze gebruiker moet een systeembeheerder van het Dataverse-exemplaar zijn. Als u deze waarde wilt vinden, opent u de [Azure Portal](https://portal.azure.com), gaat u naar **Azure Active Directory \> Gebruikers**, selecteert u de gebruiker en kopieert u vervolgens in de sectie **Identiteit** de waarde **Object-id**. |
    | Is dit de standaard CDS-omgeving voor de tenant?      | Schakel dit selectievakje in als het Dataverse-exemplaar het eerste productie-exemplaar is dat is gemaakt. Als het Dataverse-exemplaar handmatig is gemaakt, schakelt u dit selectievakje uit. |

## <a name="feedback-and-support"></a>Feedback en ondersteuning

Stuur een e-mail naar [Inzichten voor betalingen van klanten (preview)](mailto:fiap@microsoft.com) als u feedback wilt geven of ondersteuning nodig hebt.

## <a name="privacy-notice"></a>Privacyverklaring

Previews (1) bieden mogelijk minder privacy- en beveiligingsmaatregelen dan de service Dynamics 365 Finance and Operations, (2) worden niet opgenomen in de serviceovereenkomst voor deze service, (3) mogen niet worden gebruikt voor de verwerking van persoonsgegevens of andere gegevens die aan juridische of wettelijke nalevingvereisten zijn onderworpen en (4) worden slechts beperkt ondersteund.
