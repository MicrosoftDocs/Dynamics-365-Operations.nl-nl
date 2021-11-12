---
title: Randschaaleenheden implementeren op aangepaste hardware met LBD (preview)
description: In dit onderwerp wordt uitgelegd hoe u on-premises randschaaleenheden inricht door aangepaste hardware en implementatie te gebruiken die is gebaseerd op lokale bedrijfsgegevens (LBD).
author: cabeln
ms.date: 04/22/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 0ebbdaab9d6f040497d3158db2712e102b6e9aa8
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/25/2021
ms.locfileid: "7678976"
---
# <a name="deploy-edge-scale-units-on-custom-hardware-using-lbd-preview"></a>Randschaaleenheden implementeren op aangepaste hardware met LBD (preview)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)] <!--KFM: Until 11/1/2021 -->

Randschaaleenheden spelen een belangrijke rol in de gedistribueerde hybride topologie voor Supply Chain Management. In de hybride topologie kunt u werkbelastingen verdelen tussen uw Supply Chain Management-cloudhub en extra schaaleenheden in de cloud of aan de rand.

De randschaaleenheden kunnen worden geïmplementeerd door een lokale bedrijfsomgeving (LBD) [on-premises-omgeving](../../fin-ops-core/dev-itpro/deployment/on-premises-deployment-landing-page.md) te maken en deze vervolgens te configureren om als een schaaleenheid te fungeren in uw gedistribueerde hybride topologie voor Supply Chain Management. Dit wordt bereikt door de on-premises LBD-omgeving aan een Supply Chain Management-omgeving te koppelen in de cloud die is configureerd om als hub te fungeren.  

Randschaaleenheden zijn momenteel in preview. U kunt een omgeving van dit type daarom alleen gebruiken volgens de [preview-voorwaarden](https://aka.ms/scmcnepreviewterms).

In dit onderwerp wordt beschreven hoe u een on-premises LBD-omgeving instelt als een randschaaleenheid en deze vervolgens koppelt aan een hub.

## <a name="deployment-overview"></a>Overzicht van implementatie

Hier is een overzicht van de implementatiestappen.

1. **Een LBD-vak inschakelen in uw LBD-project in Microsoft Dynamics Lifecycle Services (LCS).**

    Tijdens de preview richten LBD-randschaaleenheden zich op bestaande LBD-klanten. Er wordt alleen in specifieke klantsituaties een beperkte LBD-sandbox van 60 dagen geboden.

1. **Stel een LBD-omgeving in en implementeer deze met een *lege* database**

    Gebruik LCS om de LBD-omgeving te implementeren met de nieuwste topologie en een lege database. Zie de sectie [LBD-omgeving instellen en implementeren met een lege database](#set-up-deploy) verderop in dit onderwerp voor meer informatie. U moet Supply Chain Management versie 10.0.19 gebruiken met platformupdate 43 of hoger in de hub- en schaaleenheidsomgevingen.

1. **Doelpakketten uploaden naar LBD-projectactiva in LCS.**

    Toepassings-, platform- en aanpassingspakketten voorbereiden die u in de hub- en randschaaleenheid gebruikt. Zie de sectie [Doelpakketten uploaden naar LBD-projectactiva in LCS](#upload-packages) verderop in dit onderwerp voor meer informatie.

1. **De LBD-omgeving onderhouden met de doelpakketten.**

    Via deze stap zorgt u ervoor dat dezelfde build en aanpassingen worden geïmplementeerd in de hub en de spoke. Zie de sectie [De LBD-omgeving onderhouden met doelpakketten](#service-target-packages) verderop in dit onderwerp voor meer informatie.

1. **Voltooi de configuratie van de schaaleenheid en de toewijzing van de werkbelasting.**

    Zie de sectie [Uw LBD-randschaaleenheid toewijzen aan een hub](#assign-edge-to-hub) verderop in dit onderwerp voor meer informatie.

In de overige secties van dit onderwerp vindt u meer informatie over hoe u deze stappen uitvoert.

## <a name="set-up-and-deploy-an-lbd-environment-with-an-empty-database"></a><a name="set-up-deploy"></a>Een LBD-omgeving instellen en implementeren met een lege database

Via deze stap maakt u een functionele LBD-omgeving. De omgeving heeft echter niet altijd dezelfde toepassings- en platformversies als de hub-omgeving. Bovendien ontbreken in de omgeving nog steeds de aanpassingen en is de omgeving nog niet ingeschakeld om als schaaleenheid te werken.

1. Volg de instructies in [On-premises omgevingen instellen en implementeren (Platform update 41 en hoger)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md). U moet Supply Chain Management versie 10.0.19 gebruiken met platformupdate 43 of hoger in de hub- en schaaleenheidomgevingen

    > [!IMPORTANT]
    > Lees het resterende deel van deze sectie **voordat** u de stappen in dat onderwerp uitvoert.

1. Voer het volgende script uit voordat u uw configuratie in het infrastructuurbestand\\ConfigTemplate.xml beschrijft:

    ```powershell
    .\Configure-ScriptsForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > Met dit script verwijdert u configuraties die niet nodig zijn voor de implementatie van randschaaleenheden.

1. Stel een database in met lege gegevens, zoals is beschreven in [Databases configureren](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb). Gebruik het lege data.bak-bestand voor deze stap.
1. Stel het script vóór de implementatie in. Zie [Scripts voor vóór en na de implementatie voor lokale agenten](../../fin-ops-core/dev-itpro/lifecycle-services/pre-post-scripts.md) voor meer informatie

    1. Kopieer de inhoud van de map **ScaleUnit** in **Infrastructuurscripts** naar de map **Scripts** in de opslagshare voor agentbestanden die in de omgeving is ingesteld. Een standaardpad is \\\\lbdiscsi01\\agent\\Scripts.
    2. Maak het script **PreDeployment.ps1** waarmee de scripts worden aangeroepen door de vereiste parameters te gebruiken. Het script vóór de implementatie moet in de map **Scripts** in de opslagshare voor agentbestanden worden geplaatst. Anders kan het niet worden uitgevoerd. Een standaardpad is \\\\lbdiscsi01\\agent\\Scripts\\PreDeployment.ps1.

        De inhoud van het script PreDeployment.ps1 lijkt op het volgende voorbeeld.

        ```powershell
        $agentShare = '\\lbdiscsi01\agent'
        
        Write-Output "AgentShare is set to $agentShare" 
        & $agentShare\Scripts\Configure-CloudandEdge.ps1 -AgentShare $agentShare -InstanceId '@A' -DatabaseServer 'lbdsqla01.contoso.com' -DatabaseName 'AXDB'
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

## <a name="upload-target-packages-into-lbd-project-assets-in-lcs"></a><a name="upload-packages"></a>Doelpakketten uploaden naar LBD-projectactiva in LCS.

Met deze stap bereidt u de toepassingsversie, platformversie en aanpassingen voor die worden overgebracht naar uw LBD-schaaleenheidomgeving.

1. Upload hetzelfde gecombineerde toepassings-/platformpakket dat op de hub-omgeving is toegepast naar de activabibliotheek van het on-premises LCS-project.
1. Gebruik een kopie van het aangepaste implementeerbare pakket dat op de hub-omgeving is toegepast en upload het pakket naar de activabibliotheek van het on-premises LCS-project.

## <a name="service-the-lbd-environment-with-target-packages"></a><a name="service-target-packages"></a>De LBD-omgeving onderhouden met doelpakketten.

Met deze stap stemt u de toepassingsversie, platformversie en aanpassingen in uw LBD-schaaleenheidomgeving af met de hub.

1. Onderhoud de LBD-omgeving met het gecombineerde toepassings-/platformpakket dat u in de vorige stap hebt geüpload.
1. Onderhoud de LBD-omgeving met het aangepaste implementeerbare pakket dat u in de vorige stap hebt geüpload.

    ![Onderhouden > Updates toepassen in LCS selecteren.](media/cloud_edge-LBD-LCS-ServiceLBDEnv1.png "Onderhouden > Updates toepassen in LCS selecteren")

    ![Uw aanpassingspakket selecteren.](media/cloud_edge-LBD-LCS-ServiceLBDEnv2.png "Uw aanpassingspakket selecteren")

## <a name="assign-your-lbd-edge-scale-unit-to-a-hub"></a><a name="assign-edge-to-hub"></a>Uw LBD-randschaaleenheid aan een hub toewijzen

Zolang randschaaleenheden no in preview zijn, moet u de [tools voor de implementatie en configuratie van schaaleenheden](https://github.com/microsoft/SCMScaleUnitDevTools) gebruiken die beschikbaar zijn op GitHub om uw LBD-randschaaleenheid aan een hub toe te wijzen. Via dit proces kan een LBD-configuratie functioneren als een randschaaleenheid en aan de hub worden gekoppeld. Het proces is vergelijkbaar met het configureren van een ontwikkelomgeving met één vak.

1. Download de laatste versie van [SCMScaleUnitDevTools](https://github.com/microsoft/SCMScaleUnitDevTools/releases) en pak de inhoud van het bestand uit.
1. Maak een kopie van het bestand `UserConfig.sample.xml` en geef het bestand de naam `UserConfig.xml`.
1. Maak een Microsoft Azure Active Directory (Azure AD)-toepassing in uw Azure AD-tenant, zoals wordt vermeld in de [Implementatiehandleiding voor schaaleenheid en werkbelastingen](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide#aad-application-registrations).
    1. Nadat u de toepassing hebt gemaakt, gaat u naar het formulier Azure AD-toepassingen (SysAADClientTable) in uw hub.
    1. Maak een nieuwe vermelding en stel **Client-id** in op de id van de toepassing die u hebt gemaakt. Stel **Naam** in op *ScaleUnits* en **Gebruikers-id** op *Beheerder*.

1. Maak een ADFS-toepassing (Active Directory Federation Service) zoals wordt vermeld in de [Implementatiehandleiding voor schaaleenheid en werkbelastingen](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide#adfs-application-registrations).
    1. Nadat u de toepassing hebt gemaakt, gaat u naar het formulier Azure AD-toepassingen (SysAADClientTable) in uw randschaaleenheid.
    1. Maak een nieuwe vermelding en stel **Client-id** in op de id van de toepassing die u hebt gemaakt. Stel **Gebruikers-id** in op *Beheerder*.

1. Pas het bestand `UserConfig.xml` aan.
    1. Voer onder de sectie `InterAOSAADConfiguration` de gegevens in van de Azure AD-toepassing die u eerder hebt gemaakt.
        - Voer in het element `AppId` de toepassings-id van de Azure-toepassing in.
        - Voer in het element `AppSecret` het toepassingsgeheim in van de Azure-toepassing.
        - Het element `Authority` moet de URL bevatten waarmee de beveiligingsautoriteit voor uw tenants wordt opgegeven.

        ```xml
        <InterAOSAADConfiguration>
            <AppId>8dab14f6-97b1-48e3-b51b-350b45f6ede5</AppId>
            <AppSecret>k6em-_7.lopty56TGUedDTVhtER-j_6anY1</AppSecret>
            <Authority>https://login.windows.net/contoso.onmicrosoft.com</Authority>
        </InterAOSAADConfiguration>
        ```

    1. Wijzig onder de sectie `ScaleUnitConfiguration` voor de eerste `ScaleUnitInstance` de sectie `AuthConfiguration`.
        - Voer in het element `AppId` de toepassings-id van de Azure-toepassing in.
        - Voer in het element `AppSecret` het toepassingsgeheim in van de Azure-toepassing.
        - Het element `Authority` moet de URL bevatten waarmee de beveiligingsautoriteit voor uw tenants wordt opgegeven.

        ```xml
        <AuthConfiguration>
            <AppId>8dab14f6-97b1-48e3-b51b-350b45f6ede5</AppId>
            <AppSecret>k6em-_7.lopdz.6d3DTVOtf9Lo-j_6anY1</AppSecret>
            <Authority>https://login.windows.net/contoso.onmicrosoft.com</Authority>
        </AuthConfiguration>
        ```

    1. Stel voor dezelfde `ScaleUnitInstance` ook de volgende waarden in:
        - Geef in het element `Domain` de URL van uw hub op. Voorbeeld: `https://cloudhub.sandbox.operations.dynamics.com/`
        - Zorg ervoor dat in het element `EnvironmentType` de waarde `LCSHosted` is ingesteld.

    1. Wijzig onder de sectie `ScaleUnitConfiguration` voor de tweede `ScaleUnitInstance` de sectie `AuthConfiguration`.
        - Voer in het element `AppId` de toepassings-id in van de ADFS-toepassing.
        - Voer in het element `AppSecret` het toepassingsgeheim van de ADFS-toepassing in.
        - Het element `Authority` moet de URL van uw ADFS-instantie bevatten.

        ```xml
        <AuthConfiguration>
            <AppId>26b16f25-21d8-4d36-987b-62df292895aa</AppId>
            <AppSecret>iZFfObgI6lLtY9kEbBjEFV98NqI5_YZ0e5SBcWER</AppSecret>
            <Authority>https://adfs.contoso.com/adfs</Authority>
        </AuthConfiguration>
        ```

    1. Stel voor dezelfde `ScaleUnitInstance` ook de volgende waarden in:
        - Geef in het element `Domain` de URL van uw randschaaleenheid op. Voorbeeld: https://ax.contoso.com/
        - Zorg ervoor dat in het element `EnvironmentType` de waarde LBD is ingesteld.
        - Voer in het element `ScaleUnitId` dezelfde waarde in die u hebt opgegeven voor de `InstanceId` toen u het script vóór de implementatie `Configure-CloudandEdge.ps1` configureerde.

        > [!NOTE]
        > Als u de standaard-id (@A) niet gebruikt, moet u de ScaleUnitId voor elke ConfiguredWorkload bijwerken onder de sectie Werkbelastingen.

1. Open PowerShell en ga naar de map met het bestand `UserConfig.xml`.

1. Voer het hulpprogramma uit met deze opdracht.

    ```powershell
    .\CLI.exe
    ```

    > [!NOTE]
    > Na elke actie moet u het hulpprogramma opnieuw starten.

1. Selecteer **2. Omgevingen voorbereiden voor de installatie van werkbelastingen**. Voer vervolgens de volgende stappen uit:
    1. Selecteer **1. De hub voorbereiden**.
    1. Selecteer **2. De schaaleenheid voorbereiden**.

    > [!NOTE]
    > Voer de volgende acties uit als u deze opdracht niet vanuit een schone installatie uitvoert en de opdracht mislukt:
    >
    > - Verwijder alle mappen uit de map `aos-storage` (behalve de map `GACAssemblies`).
    > - Voer de volgende SQL-opdracht uit op uw bedrijfsdatabase (AXDB):
    >
    > ```sql 
    > delete from storagefoler
    > ```

1. Voer de volgende SQL-opdrachten uit in uw bedrijfsdatabase (AXDB):

    ```sql
    delete from FEATUREMANAGEMENTMETADATA
    delete from FEATUREMANAGEMENTSTATE
    delete from NUMBERSEQUENCESCOPE
    ```

1. Controleer of het bijhouden van wijzigingen is ingeschakeld in uw bedrijfsdatabase (AXDB)
    1. Start SQL Server Management Studio (SSMS).
    1. Klik met de rechtermuisknop op uw bedrijfsdatabase (AXDB) en selecteer eigenschappen.
    1. Selecteer in het venster dat wordt geopend de optie **Wijzigingen bijhouden** en selecteer de volgende instellingen:

        - **Wijzigingen bijhouden:** *True*
        - **Retentieperiode:** *7*
        - **Retentie-eenheden:** *Dagen*
        - **Automatisch opschonen:** *True*

1. Selecteer **3. Werkbelastingen installeren** in het hulpprogramma. Voer vervolgens de volgende stappen uit:
    1. Selecteer **1. Installeren in hub**.
    1. Selecteer **2. Installeren in schaaleenheid**.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
