---
title: Randschaaleenheden implementeren op aangepaste hardware met LBD
description: In dit onderwerp wordt uitgelegd hoe u on-premises randschaaleenheden inricht door aangepaste hardware en implementatie te gebruiken die is gebaseerd op lokale bedrijfsgegevens (LBD).
author: cabeln
ms.date: 01/24/2022
ms.topic: article
ms.prod: dynamics-365
ms.service: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 37bc8678d4e04afebbebaaa893a484866a8643ce
ms.sourcegitcommit: 23588e66e25c05e989f3212ac519d7016820430a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2022
ms.locfileid: "8565542"
---
# <a name="deploy-edge-scale-units-on-custom-hardware-using-lbd"></a>Randschaaleenheden implementeren op aangepaste hardware met LBD

[!include [banner](../includes/banner.md)]

Randschaaleenheden spelen een belangrijke rol in de gedistribueerde hybride topologie voor Supply Chain Management. In de hybride topologie kunt u werkbelastingen verdelen tussen uw Supply Chain Management-cloudhub en extra schaaleenheden in de cloud of aan de rand.

De randschaaleenheden kunnen worden geïmplementeerd door een lokale bedrijfsomgeving (LBD) [on-premises-omgeving](../../fin-ops-core/dev-itpro/deployment/on-premises-deployment-landing-page.md) te maken en deze vervolgens te configureren om als een schaaleenheid te fungeren in uw gedistribueerde hybride topologie voor Supply Chain Management. Dit wordt bereikt door de on-premises LBD-omgeving aan een Supply Chain Management-omgeving te koppelen in de cloud die is configureerd om als hub te fungeren.  

In dit onderwerp wordt beschreven hoe u een on-premises LBD-omgeving instelt als een randschaaleenheid en deze vervolgens koppelt aan een hub.

## <a name="infrastructure-considerations"></a>Infrastructuuroverwegingen

Randschaaleenheden worden uitgevoerd in on-premises omgevingen, waardoor de infrastructuurvereisten redelijk vergelijkbaar zijn. Er zijn echter bepaalde verschillen waarmee rekening moet worden gehouden:

- Voor randschaaleenheden wordt geen gebruik gemaakt van Financial Reporting, waardoor er geen knooppunten voor Financial Reporting nodig zijn.
- De workloads voor productie en magazijnbeheer zijn niet rekenintensief. Daarom moet u overwegen de rekenkracht voor AOS-knooppunten dienovereenkomstig aan te passen.

## <a name="deployment-overview"></a>Overzicht van implementatie

Hier is een overzicht van de implementatiestappen.

1. **Een LBD-vak inschakelen in uw LBD-project in Microsoft Dynamics Lifecycle Services (LCS).**

1. **Stel een LBD-omgeving in en implementeer deze met een *lege* database**

    Gebruik LCS om de LBD-omgeving te implementeren met de nieuwste topologie en een lege database. Zie de sectie [LBD-omgeving instellen en implementeren met een lege database](#set-up-deploy) verderop in dit onderwerp voor meer informatie. U moet Supply Chain Management versie 10.0.21 of hoger gebruiken in de hub- en schaaleenheidsomgevingen.

1. **Doelpakketten uploaden naar LBD-projectactiva in LCS.**

    Toepassings-, platform- en aanpassingspakketten voorbereiden die u in de hub- en randschaaleenheid gebruikt. Zie de sectie [Doelpakketten uploaden naar LBD-projectactiva in LCS](#upload-packages) verderop in dit onderwerp voor meer informatie.

1. **De LBD-omgeving onderhouden met de doelpakketten.**

    Via deze stap zorgt u ervoor dat dezelfde build en aanpassingen worden geïmplementeerd in de hub en de spoke. Zie de sectie [De LBD-omgeving onderhouden met doelpakketten](#service-target-packages) verderop in dit onderwerp voor meer informatie.

1. **Voltooi de configuratie van de schaaleenheid en de toewijzing van de werkbelasting.**

    Zie de sectie [Uw LBD-randschaaleenheid toewijzen aan een hub](#assign-edge-to-hub) verderop in dit onderwerp voor meer informatie.

In de overige secties van dit onderwerp vindt u meer informatie over hoe u deze stappen uitvoert.

## <a name="set-up-and-deploy-an-lbd-environment-with-an-empty-database"></a><a name="set-up-deploy"></a>Een LBD-omgeving instellen en implementeren met een lege database

Via deze stap maakt u een functionele LBD-omgeving. De omgeving heeft echter niet altijd dezelfde toepassings- en platformversies als de hub-omgeving. Bovendien ontbreken in de omgeving nog steeds de aanpassingen en is de omgeving nog niet ingeschakeld om als schaaleenheid te werken.

1. Volg de instructies in [On-premises omgevingen instellen en implementeren (Platform update 41 en hoger)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md). U moet Supply Chain Management versie 10.0.21 of hoger gebruiken in de hub- en schaaleenheidsomgevingen. Daarnaast moet u versie 2.12.0 of hoger van de infrastructuurscripts gebruiken. 

    > [!IMPORTANT]
    > Lees het resterende deel van deze sectie **voordat** u de stappen in dat onderwerp uitvoert.

1. Voer het volgende script uit voordat u uw configuratie in het infrastructuurbestand\\ConfigTemplate.xml beschrijft:

    ```powershell
    .\Configure-ScriptsForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > Met dit script verwijdert u configuraties die niet nodig zijn voor de implementatie van randschaaleenheden.

1. Stel een database in met lege gegevens, zoals is beschreven in [Databases configureren](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb). Gebruik het lege data.bak-bestand voor deze stap.
1. Nadat u de stap [Databases configurferen](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) hebt uitgevoerd, voert u het volgende script uit om de Scale Unit Alm Orchestrator-database te configureren.

    > [!NOTE]
    > Configureer de Financial Reporting-database niet tijdens tijdens de stap [Databases configureren](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb).

    ```powershell
    .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName EdgeScaleUnit
    ```

    Het script Initialize-Database.ps1 voert de volgende acties uit:

    1. Maak een lege database met de naam **ScaleUnitAlmDb**.
    2. Wijs de gebruikers aan databaserollen toe, aan de hand van de volgende tabel.

        | Gebruiker            | Type | Databaserol |
        |-----------------|------|---------------|
        | svc-LocalAgent$ | gMSA | db\_eigenaar     |

1. Blijf de instructies volgen in [On-premises omgevingen instellen en implementeren (Platform update 41 en hoger)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md).
1. Nadat u de stap [AD FS configureren](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb) hebt voltooid, volgt u deze stappen:

    1. Maak een nieuwe AD FS-toepassing (Active Directory Federation Services) waarmee de Alm Orchestration-service kan communiceren met uw Application Object Server (AOS).

        ```powershell
        # Host URL is your DNS record\host name for accessing the AOS
        .\Create-ADFSServerApplicationForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -HostUrl 'https://ax.d365ffo.onprem.contoso.com'
        ```

    1. Maak een nieuwe Azure Active Directory (Azure AD)-toepassing waarmee de Alm Orchestration-service kan communiceren met de schaaleenheidbeheerservice.

        ```powershell
        # Example .\Create-SumAADApplication.ps1 -ConfigurationFilePath ..\ConfigTemplate.xml -TenantId '6240a19e-86f1-41af-91ab-dbe29dbcfb95' -ApplicationDisplayName 'EdgeAgent-SUMCommunication-EN01'
        .\Create-SumAADApplication.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                       -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                       -ApplicationDisplayName '<Whichever name you want the Azure AD app to have>'
        ```

1. Blijf de instructies volgen in [On-premises omgevingen instellen en implementeren (Platform update 41 en hoger)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md). Wanneer u de configuratie voor de lokale agent moet invoeren, zorg er dan voor dat u de Edge-schaaleenheidfuncties inschakelt en alle vereiste parameters opgeeft.

    ![Edge-schaaleenheidfuncties inschakelen.](media/EnableEdgeScaleUnitFeatures.png "Edge-schaaleenheidfuncties inschakelen.")

1. Stel het script vóór de implementatie in voordat u uw omgeving vanuit LCS implementeert. Zie [Scripts voor vóór en na de implementatie voor lokale agenten](../../fin-ops-core/dev-itpro/lifecycle-services/pre-post-scripts.md) voor meer informatie

    1. Kopieer het script Configure-CloudAndEdge.ps1 van de map **ScaleUnit** in **Infrastructuurscripts** naar de map **Scripts** in de opslagshare voor agentbestanden die in de omgeving is ingesteld. Een standaardpad is \\\\lbdiscsi01\\agent\\Scripts.
    2. Maak het script **PreDeployment.ps1** waarmee de scripts worden aangeroepen door de vereiste parameters te gebruiken. Het script vóór de implementatie moet in de map **Scripts** in de opslagshare voor agentbestanden worden geplaatst. Anders kan het niet worden uitgevoerd. Een standaardpad is \\\\lbdiscsi01\\agent\\Scripts\\PreDeployment.ps1.

        De inhoud van het script PreDeployment.ps1 lijkt op het volgende voorbeeld.

        ```powershell
        $agentShare = '\\lbdiscsi01\agent'
        
        Write-Output "AgentShare is set to $agentShare" 
        . $PSScriptRoot\Configure-CloudAndEdge.ps1 -AgentShare $agentShare -InstanceId '@A'
        ```

        > [!NOTE]
        > De parameter InstanceId mag niet meer dan twee tekens bevatten. Het eerste teken is @ en het tweede teken kan elke hoofdletter in het Engelse alfabet zijn.
        >
        > - Geldige waarden:
        >   - @D
        >   - @X
        > - Ongeldige waarden:
        >   - @a
        >   - @4
        >   - @#

1. Implementeer de omgeving met de nieuwste basistopologie die beschikbaar is.
1. Ga als volgt te werk nadat uw omgeving is geïmplementeerd:

    1. Voer de volgende SQL-opdrachten uit in uw bedrijfsdatabase (AXDB).

        ```sql
        ALTER TABLE dbo.NUMBERSEQUENCETABLE ENABLE CHANGE_TRACKING WITH (TRACK_COLUMNS_UPDATED = ON)
        delete from NumberSequenceTable
        delete from NumberSequenceReference
        delete from NumberSequenceScope
        delete from FeatureManagementMetadata
        delete from FeatureManagementState
        delete from SysFeatureStateV0
        ```

    1. Verhoog de maximale gelijktijdige batchsessie tot een waarde van meer dan 4.

        ```sql
        Update batchserverconfig set maxbatchsessions = '<Replace with number of concurrent batch tasks you want>'
        ```

    1. Controleer of het bijhouden van wijzigingen is ingeschakeld in uw bedrijfsdatabase (AXDB).

        1. Open SQL Server Management Studio (SSMS).
        1. Selecteer het bestand en houd deze ingedrukt (of klik met de rechtermuisknop) op uw bedrijfsdatabase (AXDB) en selecteer **Eigenschappen**.
        1. Selecteer in het venster dat verschijnt de optie **Wijzigingen bijhouden** en stel de volgende waarden in:

            - **Wijzigingen bijhouden:** *True*
            - **Retentieperiode:** *7*
            - **Retentie-eenheden:** *Dagen*
            - **Automatisch opschonen:** *True*

    1. Voeg de AD FS-toepassings-ID toe die u eerder hebt gemaakt (met het script Create-ADFSServerApplicationForEdgeScaleUnits.ps1) aan de Azure AD-toepassingentabel in uw schaaleenheid. U kunt deze stap handmatig voltooien via de gebruikersinterface (UI). U kunt het ook voltooien via de database door het volgende script te gebruiken.

        ```sql
        DECLARE @ALMOrchestratorId NVARCHAR(76) = '<Replace with the ADFS Application ID created in a previous step>';

        IF NOT EXISTS (SELECT TOP 1 1 FROM SysAADClientTable WHERE AADClientId = @ALMOrchestratorId)
        BEGIN
            INSERT INTO SysAADClientTable (AADClientId, UserId, Name, ModifiedBy, CreatedBy)
            VALUES (@ALMOrchestratorId, 'ScaleUnitManagement', 'Scale Unit Management', 'Admin', 'Admin');
        END
        ```

## <a name="set-up-an-azure-key-vault-and-an-azure-ad-application-to-enable-communication-between-scale-units"></a><a name="set-up-keyvault"></a>Een Azure-sleutelkluis en een Azure AD-toepassing instellen voor communicatie tussen schaaleenheden

1. Nadat uw omgeving is geïmplementeerd, maakt u een extra Azure AD-toepassing om vertrouwde communicatie tussen uw hub en schaaleenheid mogelijk te maken.

    ```powershell
    .\Create-SpokeToHubAADApplication.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                          -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                          -ApplicationDisplayName '<Whichever name you want the Azure AD app to have>'
    ```

1. Nadat u de toepassing hebt gemaakt, moet u een clientgeheim maken en de informatie opslaan in een Azure-sleutelkluis. Daarnaast moet u toegang verlenen tot de Azure AD-toepassing die is gemaakt, zodat deze de sleutels kan ophalen die in de sleutelkluis zijn opgeslagen. Voor uw gemak voert het volgende script automatisch alle vereiste acties uit.

    ```powershell
    .\Create-SpokeToHubAADAppSecrets.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                         -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                         -SubscriptionName '<Any subscription within your tenant>' `
                                         -ResourceGroupName '<Any resource group within your subscription>' `
                                         -KeyVaultName '<Any key vault within your resource group>' `
                                         -Location '<Any Azure location where Azure Key Vault is available>' `
                                         -LCSEnvironmentId '<The LCS environment ID of your deployed scale unit>' `
    ```

    > [!NOTE]
    > Als er geen sleutelkluis bestaat die de opgegeven waarde **KeyVaultName** heeft, maakt het script er automatisch een.

1. Voeg de Azure AD-toepassings-id toe die u zojuist gemaakt hebt (bij gebruik van het Create-SpokeToHubAADApplication.ps1 script) aan de Azure AD-toepassingentabel in uw hub. U kunt deze stap handmatig voltooien via de gebruikersinterface.

## <a name="upload-target-packages-into-lbd-project-assets-in-lcs"></a><a name="upload-packages"></a>Doelpakketten uploaden naar LBD-projectactiva in LCS.

Met deze stap bereidt u de toepassingsversie, platformversie en aanpassingen voor die worden overgebracht naar uw LBD-schaaleenheidomgeving.

1. Upload hetzelfde gecombineerde toepassings-/platformpakket dat op de hub-omgeving is toegepast naar de activabibliotheek van het on-premises LCS-project.
1. Gebruik een kopie van het aangepaste implementeerbare pakket dat op de hub-omgeving is toegepast en upload het pakket naar de activabibliotheek van het on-premises LCS-project.

## <a name="service-the-lbd-environment-with-target-packages"></a><a name="service-target-packages"></a>De LBD-omgeving onderhouden met doelpakketten.

Met deze stap stemt u de toepassingsversie, platformversie en aanpassingen in uw LBD-schaaleenheidomgeving af met de hub.

1. Onderhoud de LBD-omgeving met het gecombineerde toepassings-/platformpakket dat u in de vorige stap hebt geüpload.
1. Onderhoud de LBD-omgeving met het aangepaste implementeerbare pakket dat u in de vorige stap hebt geüpload.

    ![Updates in LCS toepassen.](media/cloud_edge-LBD-LCS-ServiceLBDEnv1.png "Updates in LCS toepassen")

    ![Uw aanpassingspakket selecteren.](media/cloud_edge-LBD-LCS-ServiceLBDEnv2.png "Uw aanpassingspakket selecteren")

## <a name="assign-your-lbd-edge-scale-unit-to-a-hub"></a><a name="assign-edge-to-hub"></a>Uw LBD-randschaaleenheid aan een hub toewijzen

U configureert en beheert de schaaleenheid voor de rand via het beheerportal voor schaaleenheden. Zie [Schaaleenheden en workloads beheren via de beheerportal voor schaaleenheden](./cloud-edge-landing-page.md#scale-unit-manager-portal) voor meer informatie.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
