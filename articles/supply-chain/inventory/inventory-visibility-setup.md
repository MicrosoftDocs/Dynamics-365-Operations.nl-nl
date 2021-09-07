---
title: Voorraadzichtbaarheid instellen
description: In dit onderwerp wordt beschreven hoe u de invoegtoepassing voor de Voorraadzichtbaarheid installeert voor Microsoft Dynamics 365 Supply Chain Management.
author: yufeihuang
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 8573fe01abb1c6092012baf85e8b7df40b74a31f
ms.sourcegitcommit: b9c2798aa994e1526d1c50726f807e6335885e1a
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/13/2021
ms.locfileid: "7343579"
---
# <a name="set-up-inventory-visibility"></a>Voorraadzichtbaarheid instellen

[!include [banner](../includes/banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

In dit onderwerp wordt beschreven hoe u de invoegtoepassing voor de Voorraadzichtbaarheid installeert voor Microsoft Dynamics 365 Supply Chain Management.

U moet de invoegtoepassing voor Voorraadzichtbaarheid installeren met behulp van Microsoft Dynamics Lifecycle Services (LCS). LCS is een portal voor samenwerking die een omgeving en een reeks regelmatig bijgewerkte services biedt waarmee u de toepassingslevensduur van uw finance and operations-apps kunt beheren.

Zie voor meer informatie [Lifecycle Services-resources](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

## <a name="inventory-visibility-prerequisites"></a>Vereisten voor Voorraadzichtbaarheid

Voordat u de Voorraadzichtbaarheid kunt installeren, moet u de volgende taken uitvoeren:

- Schaf een LCS-implementatieproject aan met minimaal één geïmplementeerde omgeving.
- Zorg ervoor dat er aan de vereisten voor het instellen van invoegtoepassingen voldaan is. Zie [Overzicht invoegtoepassingen](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) voor informatie over deze vereisten. Voor Voorraadzichtbaarheid is geen koppeling voor twee keer wegschrijven vereist.
- Neem via [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) contact op met het productteam om de volgende vereiste bestanden op te halen:

    - `InventoryServiceApplication.PackageDeployer.zip`
    - `Inventory Visibility Integration.zip` (als u een eerdere versie van Supply Chain Management uitvoert dan versie 10.0.18)

> [!NOTE]
> De landen en regio's die momenteel worden ondersteund, zijn Canada ( CCA, ECA), de Verenigde Staten (VS, EUS), de europese Unie (NEU, WEU), het Verenigd Koninkrijk (SUK, WUK) en Australië (EAU, SEAU).

Neem bij vragen over deze vereisten contact op met het productteam voor Voorraadzichtbaarheid.

## <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a>Dataverse instellen

Als u Dataverse zodanig wilt instellen dat dit met Voorraadzichtbaarheid kan worden gebruikt, dient u het hulpprogramma package deployer te gebruiken om het Voorraadzichtbaarheid-pakket te implementeren. In de volgende onderdelen wordt beschreven hoe u elk van deze taken uitvoert.

> [!NOTE]
> Momenteel worden alleen Dataverse-omgevingen ondersteund die met behulp van LCS gemaakt zijn. Als uw Dataverse-omgeving op een andere manier gemaakt is (bijvoorbeeld door het Power Apps-beheercentrum te gebruiken) en als deze aan uw Supply Chain Management-omgeving gekoppeld is, moet u eerst contact opnemen met het productteam van Voorraadzichtbaarheid om het toewijzingsprobleem te verhelpen. U kunt de invoegtoepassing Voorraadzichtbaarheid vervolgens installeren.

### <a name="migrate-from-an-old-version-of-the-dataverse-solution"></a>Migreren van een oude versie van de Dataverse-oplossing

Als u een oudere versie van de Voorraadzichtbaarheid Dataverse-oplossing geïnstalleerd hebt, gebruikt u deze instructies om de versie bij te werken. Hiervoor zijn er twee opties:

- **Optie 1:** als u Dataverse handmatig hebt ingesteld door de `Inventory Visibility Dataverse Solution_1_0_0_2_managed.zip`-oplossing te importeren, volgt u deze stappen:

    1. Download de volgende drie bestanden:

        - `Inventory Visibility Dataverse Solution_1_0_0_3_managed.zip`
        - `InventoryServiceBase_managed.cab`
        - `InventoryServiceApplication.PackageDeployer.zip`

    1. Importeer `Inventory Visibility Dataverse Solution_1_0_0_3_managed.zip` en `InventoryServiceBase_managed.cab` in Dataverse handmatig door de volgende stappen uit te voeren:

        1. Open de URL van uw Dataverse-omgeving.
        1. Open de pagina **Oplossingen**.
        1. Selecteer **Importeren**.

    1. Gebruik de package deployer-tool om het `InventoryServiceApplication.PackageDeployer.zip`-pakket te implementeren. Zie het gedeelte [Hulpprogramma package deployer voor het implementeren van het pakket](#deploy-package) later in dit onderwerp voor instructies.

- **Optie 2:** als u Dataverse installeert met behulp van het hulpprogramma package deployer, voordat u het oudere `.*PackageDeployer.zip`-pakket geïnstalleerd hebt, downloadt u `InventoryServiceApplication.PackageDeployer.zip` en voert u een update uit. Zie het gedeelte [Hulpprogramma package deployer voor het implementeren van het pakket](#deploy-package) voor instructies.

### <a name="use-the-package-deployer-tool-to-deploy-the-package"></a><a name="deploy-package"></a>Gebruik de package deployer-tool om het pakket te implementeren

1. Installeer de ontwikkelhulpprogramma's zoals beschreven in [Hulpprogramma's downloaden van NuGet](/dynamics365/customerengagement/on-premises/developer/download-tools-nuget).
1. Hef de blokkering van het `InventoryServiceApplication.PackageDeployer.zip`-bestand op, dat u vanuit de groep Teams gedownload hebt door de volgende stappen uit te voeren:

    1. Selecteer het bestand en houd deze ingedrukt (of klik met de rechtermuisknop) en selecteer **Eigenschappen**.
    1. Zoek in het dialoogvenster **Eigenschappen** in het tabblad **Algemeen** naar **Beveiliging**, selecteer **Deblokkeren** en pas de wijziging toe. Als er geen menu-item **Beveiliging** in het tabblad **Algemeen** te vinden is, is het bestand niet geblokkeerd. Ga in dat geval verder met de volgende stap.

    ![Het gedownloade bestand deblokkeren.](media/unblock-file.png "Het gedownloade bestand deblokkeren.")

1. Pak `InventoryServiceApplication.PackageDeployer.zip` uit om de volgende items te vinden:

    - `InventoryServiceApplication`-map
    - `[Content_Types].xml`-bestand
    - `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll`-bestand

1. Kopieer elk van deze items naar de `.\Tools\PackageDeployment`-map. (Deze map is aangemaakt toen u de ontwikkelaarsprogramma's installeerde.)
1. Voer `.\Tools\PackageDeployment\PackageDeployer.exe` uit en volg de instructies op uw scherm om de oplossingen te importeren.

## <a name="install-the-inventory-visibility-add-in"></a><a name="install-add-in"></a>Invoegtoepassing Voorraadzichtbaarheid installeren

Voordat u de invoegtoepassing installeert, registreert u een toepassing en voegt u een clientgeheim toe aan Azure Active Directory (Azure AD) via uw Azure-abonnement. Zie [Een toepassing registreren](/azure/active-directory/develop/quickstart-register-app) en [Een clientgeheim toevoegen](/azure/active-directory/develop/quickstart-register-app#add-a-certificate) voor instructies. Zorg ervoor dat u de waarden **Toepassings-ID**, **Clientgeheim** en **Tenant-ID** noteert, omdat u ze later nodig hebt.

Nadat u een toepassing geregistreerd hebt en een clientgeheim aan Azure AD hebt toegevoegd, volgt u deze stappen om de invoegtoepassing voor Voorraadzichtbaarheid te installeren.

1. Meld u aan bij [LCS](https://lcs.dynamics.com/Logon/Index).
1. Selecteer op de startpagina het project waar uw omgeving is geïmplementeerd.
1. Selecteer op de projectpagina de omgeving waarin u de invoegtoepassing wilt installeren.
1. Schuif op de omgevingspagina naar beneden tot u de sectie **invoegtoepassingen voor omgeving** ziet in de **Power Platform Integratie**-sectie. Hier kunt u de Dataverse-omgevingsnaam vinden.
1. Selecteer in de sectie **Invoegtoepassingen voor omgeving** de optie **Een nieuwe invoegtoepassing installeren**.

    ![Omgevingspagina in LCS](media/inventory-visibility-environment.png "Omgevingspagina in LCS")

1. Selecteer de koppeling **Een nieuwe invoegtoepassing installeren**. Er wordt een lijst met beschikbare invoegtoepassingen weergegeven.
1. Selecteer **Voorraadzichtbaarheid** in de lijst.
1. Stel daarna de volgende velden in voor uw omgeving:

    - **AAD-toepassing (client) ID** – voer de Azure AD ID in van de toepassingsclient die u eerder aangemaakt en genoteerd hebt.
    - **AAD tenant ID** – Voer de tenant-ID in die u eerder hebt genoteerd.

    ![Pagina voor invoegtoepassingen installeren](media/inventory-visibility-setup.png "Pagina voor invoegtoepassingen instellen")

1. Ga akkoord met de voorwaarden door het selectievakje **Voorwaarden** in te schakelen.
1. Selecteer **Installeren**. De status van de invoegtoepassing wordt weergegeven als **Wordt geïnstalleerd**. Nadat de installatie voltooid is, vernieuwt u de pagina. De status moet worden gewijzigd in **Geïnstalleerd**.

## <a name="uninstall-the-inventory-visibility-add-in"></a><a name="uninstall-add-in"></a>Invoegtoepassing Voorraadzichtbaarheid deïnstalleren

Als u de installatie van de invoegtoepassing voor Voorraadzichtbaarheid ongedaan wilt maken, selecteert u **Deïnstalleren** op de LCS-pagina. Als u de installatie ongedaan maakt, wordt de invoegtoepassing voor Voorraadzichtbaarheid beëindigd, wordt de invoegtoepassing voor LCS ongedaan gemaakt en worden tijdelijke gegevens verwijderd die in de cache van de invoegtoepassing voor voorraadzichtbaarheid opgeslagen zijn. De primaire voorraadgegevens die in uw Dataverse-abonnement opgeslagen zijn, worden echter niet verwijderd.

Als u de voorraadgegevens die in uw Dataverse-abonnement zijn opgeslagen wilt deïnstalleren, opent u [Power Apps](https://make.powerapps.com), selecteert u **Omgeving** in de navigatiebalk en selecteert u de Dataverse-omgeving die aan uw LCS-omgeving gekoppeld is. Ga vervolgens naar **Oplossingen** en verwijder de volgende vijf oplossingen:

- Ankeroplossing voor de toepassing Voorraadzichtbaarheid in Dynamics 365-oplossingen
- Oplossing voor Dynamics 365 FNO SCM Inventory Visibility-toepassingen
- Configuratie van inventarisservice
- Zelfstandige voorraadzichtbaarheid
- Basisoplossing voor Dynamics 365 FNO SCM Inventory Visibility

Nadat u deze oplossingen hebt verwijderd, worden de gegevens die in tabellen zijn opgeslagen ook verwijderd.

## <a name="set-up-supply-chain-management"></a><a name="setup-dynamics-scm"></a>Supply Chain Management instellen

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>Het integratiepakket voor voorraadzichtbaarheid implementeren

Als u Supply Chain Management versie 10.0.17 of eerder uitvoert, neemt u contact op met het ondersteuningsteam voor voorraadzichtbaarheid op [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) om het pakketbestand op te halen. Implementeer het pakket vervolgens in LCS.

> [!NOTE]
> Als er tijdens de implementatie een fout optreedt omdat de versies niet overeenkomen, moet u het X++-project handmatig in uw ontwikkelomgeving importeren. Maak vervolgens het implementeerbare pakket in uw ontwikkelomgeving en implementeer dit in uw productieomgeving.
>
> De code is opgenomen in Supply Chain Management versie 10.0.18. Als u die versie of een latere versie uitvoert, is implementatie niet vereist.

Zorg ervoor dat de volgende functies zijn ingeschakeld in uw Supply Chain Management-omgeving. (Standaard zijn deze ingeschakeld.)

| Beschrijving van functie | Codeversie | Klasse in-/uitschakelen |
|---|---|---|
| Het gebruik van voorraaddimensies in de tabel InventSum in- of uitschakelen      | 10.0.11 | InventUseDimOfInventSumToggle      |
| Het gebruik van voorraaddimensies in de tabel InventSumDelta in- of uitschakelen | 10.0.12 | InventUseDimOfInventSumDeltaToggle |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a>Integratie van voorraadzichtbaarheid instellen

1. Open in Supply Chain Management de werkruimte **[Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** en schakel de functie *Integratie van voorraadzichtbaarheid* in.
1. Ga naar **Voorraadbeheer \> Instellen \> Parameters voor integratie van voorraadzichtbaarheid** en voer de URL in van de omgeving in waarin u Voorraadzichtbaarheid uitvoert. Zie [Het service-eindpunt vinden](inventory-visibility-power-platform.md#get-service-endpoint) voor meer informatie.
1. Ga naar **Voorraadbeheer \> Periodiek \> Integratie van voorraadzichtbaarheid** en schakel de taak in. Alle gebeurtenissen voor voorraadwijziging van Supply Chain Management worden nu geboekt naar Voorraadzichtbaarheid.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
