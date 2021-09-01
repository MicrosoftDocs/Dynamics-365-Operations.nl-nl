---
title: Invoegtoepassing Voorraadzichtbaarheid
description: In dit onderwerp wordt beschreven hoe u de invoegtoepassing voor de zichtbaarheid van de voorraad installeert en configureert voor Dynamics 365 Supply Chain Management.
author: sherry-zheng
ms.date: 10/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-10-26
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 8faae53f66c069c53609dee72fa30ca18a22c9eb8a86b4669c745c00976af34d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742699"
---
# <a name="inventory-visibility-add-in"></a>Invoegtoepassing Voorraadzichtbaarheid

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]
[!INCLUDE [cc-data-platform-banner](../../includes/cc-data-platform-banner.md)]

De invoegtoepassing voor de zichtbaarheid van de voorraad is een onafhankelijke en zeer schaalbare microservice waarmee real-time tracking van voorhanden voorraad wordt ingeschakeld om een globale weergave van de voorraadzichtbaarheid te genereren.

Alle informatie die betrekking heeft op de voorhanden voorraad, wordt in bijna real-time met behulp van SQL-integratie op laag niveau geëxporteerd naar de service. Externe systemen openen de service via RESTful API's om informatie over voorhanden voorraad voor bepaalde sets dimensies op te vragen, waardoor een lijst met beschikbare voorhanden posities wordt opgehaald.

Voorraadzichtbaarheid is een microservice die is gebouwd op Microsoft Dataverse, wat betekent dat u deze kunt uitbreiden door Power Apps te bouwen en Power BI toe te passen voor aangepaste functionaliteit om aan uw zakelijke vereisten te voldoen. Het is ook mogelijk om de index te upgraden om voorraadquery's uit te voeren.

Voorraadzichtbaarheid bevat configuratieopties waarmee de service kan worden geïntegreerd met systemen van derden. De service ondersteunt de gestandaardiseerde voorraaddimensie, aangepaste uitbreidbaarheid en gestandaardiseerde, configureerbare berekende hoeveelheden.

In dit onderwerp wordt beschreven hoe u de invoegtoepassing voor voorraadzichtbaarheid installeert en configureert voor Dynamics 365 Supply Chain Management en hoe u de API (Application Programming Interface) ervan gebruikt.

## <a name="install-the-inventory-visibility-add-in"></a>Invoegtoepassing Voorraadzichtbaarheid installeren

U moet de invoegtoepassing voor voorraadzichtbaarheid installeren met behulp van Microsoft Dynamics Lifecycle Services (LCS). LCS is een portal voor samenwerking die een omgeving en een reeks regelmatig bijgewerkte services biedt waarmee u de toepassingslevensduur van uw Dynamics 365 Finance and Operations-apps kunt beheren.

Zie voor meer informatie [Lifecycle Services-resources](../../fin-ops-core/dev-itpro/lifecycle-services/lcs.md).

### <a name="inventory-visibility-add-in-prerequisites"></a>Vereisten voor invoegtoepassing Voorraadzichtbaarheid

Voordat u de invoegtoepassing voor voorraadzichtbaarheid kunt installeren, moet u het volgende doen:

- Schaf een LCS-implementatieproject aan met minimaal één geïmplementeerde omgeving.
- Zorg ervoor dat aan de vereisten voor het instellen van invoegvoegingen die beschikbaar zijn in het [Overzicht van invoegvoegingen](../../fin-ops-core/dev-itpro/power-platform/add-ins-overview.md) is voldaan. Voor Voorraadzichtbaarheid is geen koppeling voor twee keer wegschrijven vereist.
- Neem contact op met het team op [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) om de volgende drie vereiste bestanden op te halen:
  - `Inventory Visibility Dataverse Solution.zip`
  - `Inventory Visibility Configuration Trigger.zip`
  - `Inventory Visibility Integration.zip` (als u een eerdere versie van Supply Chain Management uitvoert dan versie 10.0.18)
- U kunt ook contact opnemen met het Voorraadzichtbaarheid-team op [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) voor de Package Deployer-pakketten. Deze pakketten kunnen worden gebruikt door een officieel hulpprogramma voor de implementatie van pakketten.
  - `InventoryServiceBase.PackageDeployer.zip`
  - `InventoryServiceApplication.PackageDeployer.zip` (dit pakket bevat alle wijzigingen in het `InventoryServiceBase`-pakket plus extra onderdelen van de gebruikersinterface)
- Volg de instructies in [Quickstart: registreer een toepassing bij het Microsoft-identiteitsplatform](/azure/active-directory/develop/quickstart-register-app) om een toepassing te registreren en een clientgeheim aan AAD toe te voegen in uw Azure-abonnement.
  - [Een toepassing registreren](/azure/active-directory/develop/quickstart-register-app)
  - [Een clientgeheim toevoegen](/azure/active-directory/develop/quickstart-register-app#add-a-certificate)
  - De **Toepassings-id (client)**, **Clientgeheim** en **Tenant-id** worden in de volgende stappen gebruikt.

> [!NOTE]
> De landen en regio's die momenteel worden ondersteund, zijn Canada, de Verenigde Staten en de Europese Unie (EU).

Als u vragen hebt over deze vereisten, neemt u contact op met het productteam voor voorraadzichtbaarheid.

### <a name="set-up-dataverse"></a><a name="setup-microsoft-dataverse"></a>Dataverse instellen

Als u Dataverse wilt instellen voor gebruik met Voorraadzichtbaarheid, moet u eerst de vereisten voorbereiden en vervolgens bepalen of u Dataverse wilt instellen met het hulpprogramma Package Deployer of door de oplossingen handmatig te importeren (u hoeft niet beide te doen). Installeer vervolgens de invoegtoepassing Voorraadzichtbaarheid. In de volgende subsecties wordt beschreven hoe u elk van deze taken uitvoert.

#### <a name="prepare-dataverse-prerequisites"></a>Vereisten Dataverse voorbereiden

Voordat u een Dataverse gaat instellen, voegt u als volgt een serviceprincipe toe aan uw tenants:

1. Installeer Azure AD PowerShell Module v2, zoals beschreven in [Azure Active Directory PowerShell for Graph installeren](/powershell/azure/active-directory/install-adv2).

1. Voer de volgende PowerShell-opdracht uit:

    ```powershell
    Connect-AzureAD # (open a sign in window and sign in as a tenant user)
    
    New-AzureADServicePrincipal -AppId "3022308a-b9bd-4a18-b8ac-2ddedb2075e1" -DisplayName "d365-scm-inventoryservice"
    ```

#### <a name="set-up-dataverse-using-the-package-deployer-tool"></a>Dataverse instellen met het hulpprogramma Package Deployer

Als aan de vereisten is voldaan, gebruikt u de volgende procedure als u deze Dataverse wilt instellen met het hulpprogramma Package Deployer. Zie het volgende gedeelte voor informatie over het handmatig importeren van de oplossingen (niet beide methoden gebruiken).

1. Installeer ontwikkelhulpprogramma's zoals beschreven in [Hulpprogramma's downloaden van NuGet](/dynamics365/customerengagement/on-premises/developer/download-tools-nuget).

1. Kies het pakket `InventoryServiceBase` of `InventoryServiceApplication` afhankelijk van de vereisten van uw bedrijf.

1. De oplossingen importeren:
    1. Voor het `InventoryServiceBase`-pakket:
        - Pak `InventoryServiceBase.PackageDeployer.zip` uit.
        - Zoek map `InventoryServiceBase`, bestand `[Content_Types].xml`, bestand `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll`, bestand `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config` en bestand `Microsoft.Dynamics.InventoryServiceBase.PackageExtension.dll.config`. 
        - Kopieer elk van deze mappen en bestanden naar de map `.\Tools\PackageDeployment` die is gemaakt toen u de ontwikkelhulpprogramma's installeerde.
    1. Voor het `InventoryServiceApplication`-pakket:
        - Pak `InventoryServiceApplication.PackageDeployer.zip` uit.
        - Zoek map `InventoryServiceApplication`, bestand `[Content_Types].xml`, bestand `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll`, bestand `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config` en bestand `Microsoft.Dynamics.InventoryServiceApplication.PackageExtension.dll.config`.
        - Kopieer elk van deze mappen en bestanden naar de map `.\Tools\PackageDeployment` die is gemaakt toen u de ontwikkelhulpprogramma's installeerde.
    1. Voer `.\Tools\PackageDeployment\PackageDeployer.exe` uit. Volg de instructies op uw scherm om de oplossingen te importeren.

1. Wijs beveiligingsrollen toe aan de gebruiker van de toepassing.
    1. Open de URL van uw Dataverse-omgeving.
    1. Ga naar **Geavanceerde instelling \> Systeem \> Beveiliging \> Gebruikers** en zoek de gebruiker met de naam **#InventoryVisibility**.
    1. Selecteer **Rol toewijzen** en selecteer vervolgens **Systeembeheerder**. Als er een rol is met de naam **Common Data Service-gebruiker**, selecteert u ook deze rol.

#### <a name="set-up-dataverse-manually-by-importing-solutions"></a>Handmatig Dataverse instellen door oplossingen te importeren

Als aan de vereisten is voldaan, gebruikt u de volgende procedure als u deze Dataverse wilt instellen door oplossingen handmatig te importeren. Zie het vorige gedeelte voor meer informatie over het gebruik van het hulpprogramma Package Deployer (niet beide methoden gebruiken).

1. Een toepassingsgebruiker voor Voorraadzichtbaarheid maken in Dataverse:

    1. Open de URL van uw Dataverse-omgeving.
    1. Ga naar **Geavanceerde instellingen \> Systeem \> \> Gebruikers** en maak een toepassingsgebruiker. Gebruik het weergavemenu om de paginaweergave te wijzigen in **Toepassingsgebruikers**.
    1. Selecteer **Nieuw**. Stel de toepassings-id in op *3022308a-b9bd-4a18-b8ac-2ddedb2075e1*. (De object-id wordt automatisch geladen wanneer u de wijzigingen opslaat.) U kunt de naam aanpassen. U kunt de naam bijvoorbeeld wijzigen in *Voorraadzichtbaarheid*. Wanneer u klaar bent, selecteert u **Opslaan**.
    1. Selecteer **Rol toewijzen** en selecteer vervolgens **Systeembeheerder**. Als er een rol is met de naam **Common Data Service-gebruiker**, selecteert u ook deze rol.

    Zie [Een toepassingsgebruiker maken](/power-platform/admin/create-users-assign-online-security-roles#create-an-application-user) voor meer informatie.

1. Als de standaardtaal van Dataverse niet **Engels** is:

    1. Ga naar **Geavanceerde instelling \> Beheer \> Talen**.
    1. Selecteer **Engels (LanguageCode=1033)** en selecteer **Toepassen**.

1. Het bestand `Inventory Visibility Dataverse Solution.zip` met de gerelateerde entiteiten van de Dataverse-configuratie en Power Apps importeren:

    1. Ga naar de pagina **Oplossingen**.
    1. Selecteer **Importeren**.

1. De triggerstroom voor de configuratie-upgrade importeren:

    1. Ga naar de pagina Microsoft Flow.
    1. Zorg ervoor dat de verbinding met de naam *Dataverse (verouderd)* bestaat. (Als deze verbinding niet bestaat, maakt u deze.)
    1. Importeer het bestand `Inventory Visibility Configuration Trigger.zip`. Nadat dit bestand is geïmporteerd, wordt de trigger weergegeven onder **Mijn stromen**.
    1. Initialiseer de volgende vier variabelen op basis van de omgevingsgegevens:

        - Tenant-id van Azure
        - Client-id van de Azure-toepassing
        - Client-geheim van de Azure-toepassing
        - Eindpunt van voorraadzichtbaarheid

            Zie de sectie [Integratie van voorraadzichtbaarheid instellen](#setup-inventory-visibility-integration) verder op in dit onderwerp voor meer informatie over deze variabele.

        ![Configuratietrigger.](media/configuration-trigger.png "Configuratietrigger")

    1. Selecteer **Inschakelen**.

### <a name="install-the-add-in"></a><a name="install-add-in"></a>De invoegtoepassing installeren

Om de invoegtoepassing voor voorraadzichtbaarheid te installeren, moet u het volgende doen:

1. Meld u aan bij de [Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index)-portal.
1. Selecteer op de startpagina het project waar uw omgeving is geïmplementeerd.
1. Selecteer op de projectpagina de omgeving waarin u de invoegtoepassing wilt installeren.
1. Schuif op de omgevingspagina naar beneden tot u de sectie **Invoegvoegingen voor omgeving** ziet in de sectie **Power Platform-Integratie**, waar u de naam van de Dataverse-omgeving kunt vinden.
1. Selecteer in de sectie **Invoegtoepassingen voor omgeving** de optie **Een nieuwe invoegtoepassing installeren**.

    ![De omgevingspagina in LCS.](media/inventory-visibility-environment.png "De omgevingspagina in LCS")

1. Selecteer de koppeling **Een nieuwe invoegtoepassing installeren**. Er wordt een lijst met beschikbare invoegtoepassingen geopend.
1. Selecteer **Voorraadzichtbaarheid** in de lijst.
1. Voer waarden in voor de volgende velden voor uw omgeving:

    - **Id AAD-toepassing (client)**
    - **AAD-tenant-id**

    ![Toevoegen in installatiepagina.](media/inventory-visibility-setup.png "Instellingspagina invoegtoepassing")

1. Ga akkoord met de voorwaarden door het selectievakje **Voorwaarden** in te schakelen.
1. Selecteer **Installeren**. De status van de invoegtoepassing wordt weergegeven als **Wordt geïnstalleerd**. Na voltooiing vernieuwt u de pagina zodat de status wordt gewijzigd in **Geïnstalleerd**.

### <a name="uninstall-the-add-in"></a><a name="uninstall-add-in"></a>De invoegtoepassing verwijderen

Selecteer **Verwijderen** als u de invoegtoepassing wilt verwijderen. Wanneer u LCS vernieuwt, wordt de invoegtoepassing Voorraadzichtbaarheid verwijderd. Met het verwijderingsproces wordt de registratie van de invoegtoepassing verwijderd en wordt ook een taak gestart om alle bedrijfsgegevens te verwijderen die in de service zijn opgeslagen.

## <a name="consume-on-hand-inventory-data-from-supply-chain-management"></a>Gegevens van voorhanden voorraad verbruiken vanuit Supply Chain Management

### <a name="deploy-the-inventory-visibility-integration-package"></a><a name="deploy-inventory-visibility-package"></a>Het integratiepakket voor voorraadzichtbaarheid implementeren

Als u Supply Chain Management versie 10.0.17 of eerder uitvoert, neemt u contact op met het ondersteuningsteam voor voorraadzichtbaarheid op [inventvisibilitysupp@microsoft.com](mailto:inventvisibilitysupp@microsoft.com) om het pakketbestand op te halen. Implementeer het pakket vervolgens in LCS.

> [!NOTE]
> Als er tijdens de implementatie een fout optreedt omdat de versies niet overeenkomen, moet u het X++-project handmatig in uw ontwikkelomgeving importeren. Maak vervolgens het implementeerbare pakket in uw ontwikkelomgeving en implementeer dit in uw productieomgeving.
> 
> De code is opgenomen in Supply Chain Management versie 10.0.18. Als u die versie of een latere versie uitvoert, is implementatie niet vereist.

Zorg ervoor dat de volgende functies zijn ingeschakeld in uw Supply Chain Management-omgeving. (Standaard zijn deze ingeschakeld.)

| Beschrijving van functie | Codeversie | Klasse in-/uitschakelen |
|---|---|---|
| Het gebruik van voorraaddimensies in de tabel InventSum in- of uitschakelen | 10.0.11 | InventUseDimOfInventSumToggle |
| Het gebruik van voorraaddimensies in de tabel InventSumDelta in- of uitschakelen | 10.0.12 | InventUseDimOfInventSumDeltaToggle |

### <a name="set-up-inventory-visibility-integration"></a><a name="setup-inventory-visibility-integration"></a>Integratie van voorraadzichtbaarheid instellen

1. Open in Supply Chain Management de werkruimte **[Functiebeheer](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** en schakel de functie **Integratie van voorraadzichtbaarheid** in.
1. Ga naar **Voorraadbeheer \> Instellen \> Parameters voor integratie van voorraadzichtbaarheid** en voer de URL in van de omgeving in waarin u Voorraadzichtbaarheid uitvoert.

    Zoek de Azure-regio van uw LCS-omgeving op en voer vervolgens de URL in. De URL heeft de volgende notatie:

    `https://inventoryservice.<RegionShortName>-il301.gateway.prod.island.powerapps.com`

    Als u bijvoorbeeld in Europa bent, heeft uw omgeving een van de volgende URL's:

    - `https://inventoryservice.neu-il301.gateway.prod.island.powerapps.com`
    - `https://inventoryservice.weu-il301.gateway.prod.island.powerapps.com`

    De volgende regio's zijn momenteel niet beschikbaar.

    | Azure-regio | Korte naam regio |
    |---|---|
    | Australië - oost | eau |
    | Australië - zuidoost | seau |
    | Canada - centraal | cca |
    | Canada - oost | eca |
    | Noord-Europa | neu |
    | West-Europa | weu |
    | VS - oost | eus |
    | VS - west | wus |

1. Ga naar **Voorraadbeheer \> Periodiek \> Integratie van voorraadzichtbaarheid** en schakel de taak in. Alle gebeurtenissen voor voorraadwijziging van Supply Chain Management worden nu geboekt naar Voorraadzichtbaarheid.

## <a name="the-inventory-visibility-add-in-public-api"></a><a name="inventory-visibility-public-api"></a>De openbare API-invoegtoepassing Voorraadzichtbaarheid

De openbare REST API van de invoegtoepassing Voorraadzichtbaarheid biedt verschillende specifieke eindpunten voor integratie. Deze ondersteunt drie hoofdinteractietypen:

- Wijzigingen in de voorhanden voorraad naar de invoegtoepassing boeken vanuit een extern systeem
- Huidige voorhanden hoeveelheden opvragen vanuit een extern systeem
- Automatische synchronisatie met voorhanden Supply Chain Management-voorraad

Automatische synchronisatie maakt geen deel uit van de openbare API. In plaats daarvan wordt de automatisch synchronisatie op de achtergrond verwerkt voor omgevingen waarin de Invoegvoeging Voorraadzichtbaarheid is ingeschakeld.

### <a name="authentication"></a><a name="inventory-visibility-authentication"></a>Authenticatie

Het platformbeveiligingstoken wordt gebruikt om de invoegvoeging Voorraadzichtbaarheid aan te roepen. U moet daarom een *Azure Active Directory (Azure AD)-token* genereren met de Azure AD-toepassing. Vervolgens moet u het Azure AD-token gebruiken om het *toegangstoken* op te halen van de beveiligingsservice.

Ga als volgt te werk om een beveiligingsservicetoken te verkrijgen:

1. Meld u aan bij Azure Portal en gebruik het token om `clientId` en `clientSecret` voor uw Supply Chain Management-toepassing te zoeken.
1. Haal een Azure Active Directory-token (`aadToken`) op door een HTTP-aanvraag met de volgende eigenschappen in te dienen:
    - **URL** - `https://login.microsoftonline.com/${aadTenantId}/oauth2/token`
    - **methode** - `GET`
    - **Inhoud hoofdtekst (formuliergegevens)**:

        | key | waarde |
        | --- | --- |
        | client_id | ${aadAppId} |
        | client_secret | ${aadAppSecret} |
        | grant_type | client_credentials |
        | resource | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |
1. U moet als reactie een `aadToken` ontvangen, zoals in het volgende voorbeeld.

    ```json
    {
        "token_type": "Bearer",
        "expires_in": "3599",
        "ext_expires_in": "3599",
        "expires_on": "1610466645",
        "not_before": "1610462745",
        "resource": "0cdb527f-a8d1-4bf8-9436-b352c68682b2",
        "access_token": "eyJ0eX...8WQ"
    }
    ```

1. Formuleer een JSON-aanvraag die op het volgende lijkt:

    ```json
    {
        "grant_type": "client_credentials",
        "client_assertion_type":"aad_app",
        "client_assertion": "{Your_AADToken}",
        "scope":"https://inventoryservice.operations365.dynamics.com/.default",
        "context": "5dbf6cc8-255e-4de2-8a25-2101cd5649b4",
        "context_type": "finops-env"
    }
    ```

    Hierin:
    - De waarde `client_assertion` moet het in de vorige stap ontvangen `aadToken` zijn.
    - De waarde `context` moet de omgevings-ID zijn waarin u de invoegtoepassing wilt implementeren.
    - Stel alle andere waarden in zoals in het voorbeeld wordt weergegeven.

1. Dien een HTTP-aanvraag in met de volgende eigenschappen:
    - **URL** - `https://securityservice.operations365.dynamics.com/token`
    - **methode** - `POST`
    - **HTTP-header**: neem de API-versie op (sleutel is `Api-Version` en waarde is `1.0`)
    - **Inhoud hoofdtekst**: neem de JSON-aanvraag op die u in de vorige stap hebt gemaakt.

1. U ontvangt als reactie een `access_token`. Dit is wat u nodig hebt als Bearer-token voor het aanroepen van de Voorraadzichtbaarheid-API. Hier volgt een voorbeeld.

    ```json
    {
        "access_token": "{Returned_Token}",
        "token_type": "bearer",
        "expires_in": 1200
    }
    ```

### <a name="sample-request"></a><a name="inventory-visibility-sample-request"></a>Voorbeeldaanvraag

Ter referentie is hier een voorbeeld-HTTP-aanvraag, waarin u alle hulpmiddelen of programmeertaal kunt gebruiken om deze aanvraag te verzenden, zoals ``Postman``.

```json
# Url
# replace {RegionShortName} and {EnvironmentId} with your value
https://inventoryservice.{RegionShortName}-il301.gateway.prod.island.powerapps.com/api/environment/{EnvironmentId}/onhand

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "id-bike-0001",
    "organizationId": "usmf",
    "productId": "Bike",
    "quantities": {
        "pos": {
            "inbound": 5
        }  
    },
    "dimensions": {
        "SizeId": "Small",
        "ColorId": "Red",
        "SiteId": "1",
        "LocationId": "11"
    }
}
```

### <a name="configure-the-inventory-visibility-api"></a><a name="inventory-visibility-configuration"></a>De Voorraadzichtbaarheid-API configureren

Voordat u de service gaat gebruiken, moet u de configuraties uitvoeren die in de volgende subsecties worden beschreven. De configuratie kan variëren afhankelijk van de details van uw omgeving. Deze bevat hoofdzakelijk vier delen:

- [Partitionering](#partitioning)
- [Dimensieconfiguraties](#dimension-configurations)
- [Bezig met indexeren](#indexing)
- [Aangepaste meting](#custom-measurement)

#### <a name="partitioning"></a>Partitionering

Het partitioneren kan de prestaties van de API voor Voorraadzichtbaarheid aanzienlijk beïnvloeden. Het is een goed idee om een schema te definiëren waarmee kleine groeperingen van gegevens mogelijk zijn, terwijl er toch betekenisvolle gegevensquery's kunnen worden uitgevoerd.

De `organizationId` (`dataAreaId` in Supply Chain Management) zal altijd deel uitmaken van de partitionering en Voorraadzichtbaarheid is standaard ingesteld op partitioneren op dimensies als *Site + locatie*. Dit betekent dat er altijd query's voor de service moeten worden uitgevoerd met deze dimensies gedefinieerd in de filters.

> [!NOTE]
> *Site* en *Locatie* zijn twee algemene standaarddimensies in Voorraadzichtbaarheid. In Supply Chain Management worden deze dimensies *Site* (`InventSiteId`) en *Magazijn* (`InventLocationId`) genoemd.

### <a name="dimension-configurations"></a>Dimensieconfiguraties

In Voorraadzichtbaarheid wordt een lijst met algemene standaarddimensies geboden waarmee de integratie met meerdere bronsystemen wordt mogelijk gemaakt.

In de volgende tabel worden de voorraaddimensies weergegeven die de standaarddimensienamen zijn in Voorraadzichtbaarheid.

| Dimensietype | Dimensienaam |
|---|---|
| Artikel | `ColorId` |
| Artikel | `SizeId` |
| Artikel | `StyleId` |
| Artikel | `ConfigId` |
| Tracering | `BatchId` |
| Tracering | `SerialId` |
| Locatie | `LocationId` |
| Locatie | `SiteId` |
| Voorraadstatus | `StatusId` |
| Magazijnspecifiek | `WMSLocationId` |
| Magazijnspecifiek | `WMSPalletId` |
| Magazijnspecifiek | `LicensePlateId` |

> [!NOTE]
> Het dimensietype vermeld in de vorige tabel is alleen ter referentie. U hoeft het dimensietype niet te definiëren in Voorraadzichtbaarheid.

Als er een aangepaste dimensie bestaat en naar een standaardwaarde moet stromen bij verbruik door Voorraadzichtbaarheid, kunt u de naam **Aangepaste dimensie** in Voorraadzichtbaarheid configureren.

Externe systemen hebben toegang tot Voorraadzichtbaarheid via RESTful API's waarmee gegevens van voorhanden voorraad over bepaalde sets met dimensies kunnen worden opgevraagd. Voor de integratie kunt u met Voorraadzichtbaarheid de *gegevensbron van het externe kanaal* en de brondimensie naar de *doeldimensies* configureren in Voorraadzichtbaarheid.

De doeldimensies moeten een van de volgende zijn:

- Standaarddimensies in Voorraadzichtbaarheid
- Aangepaste dimensies

Het doel van dimensieconfiguratie is het standaardiseren van de integratie met meerdere systemen voor de query voor dimensies en de boekingsgebeurtenis met dimensies.

#### <a name="indexing"></a>Bezig met indexeren

Meestal is de query voor de voorhanden voorraad niet alleen op het hoogste niveau 'totaal', maar wilt u mogelijk de resultaten bekijken die zijn samengevoegd op basis van de voorraaddimensies.

Voorraadzichtbaarheid is flexibel omdat u de indexen kunt instellen die zijn gebaseerd op de dimensie of de combinatie van de dimensies.

> [!NOTE]
> Op dit moment kunt u maximaal vijf indexen configureren. U moet voorafgaand aan de implementatie zorgvuldig overwegen welke dimensie of dimensiecombinatie u gaat gebruiken om er zeker van te zijn dat deze aan uw bedrijfsbehoeften voldoet. Als u bijvoorbeeld als volgt producten wilt opvragen:

- Vraag de geaggregeerde voorhanden producten op basis van de dimensies *Kleur* en *Grootte* op.
- In sommige gevallen wilt u alleen in totaal een query voor het product uitvoeren.

U zou twee indexen hebben die als volgt zijn gedefinieerd:

- `["ColorId", "SizeId"]`
- `[]`

Het lege haakje aggregeert op basis van de product-ID binnen de partitie.

De indexering bepaalt hoe u de resultaten kunt groeperen op basis van de `groupBy`-queryinstelling. Als u in dit geval geen `groupBy`-waarden definieert, krijgt u totalen op `productid`. Als u `groupBy` als `groupBy=ColorId&groupBy=SizeId` definieert, worden er meerdere regels als resultaat gegeven, op basis van de verschillende combinaties van kleur en grootte in het systeem.

U kunt uw querycriteria in de aanvraagbody plaatsen.

Hier volgt een voorbeeldquery voor het product met de combinatie kleur en grootte.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct1", "MyProduct2"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

Voor het veld `filters` worden momenteel alleen meerdere waarden voor `ProductId` ondersteund. Als `ProductId` een lege matrix is, worden alle producten opgevraagd.

#### <a name="custom-measurement"></a>Aangepaste meting

De standaardmetingshoeveelheden worden gekoppeld aan Supply Chain Management. Maar mogelijk wilt u een hoeveelheid hebben die bestaat uit een combinatie van de standaardmetingen. Hiervoor kunt u een configuratie van aangepaste hoeveelheden hebben, die worden toegevoegd aan de uitvoer van de query's voor voorhanden voorraad.

Met deze functie kunt u een set maateenheden definiëren die wordt toegevoegd, en/of een set maateenheden die wordt afgetrokken, zodat de aangepaste meting wordt gevormd.

Met de volgende queryvoorwaarde bijvoorbeeld configureert u de aangepaste metingshoeveelheid als `MyCustomAvailableforReservation` om te worden verbruikt door het verbruikssysteem.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            }
        }
    }
]

```



| Verbruikssysteem | Berekende meters | Gegevensbron | Modificator | Berekeningstype modificator |
|---|---|---|---|---|
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `availphysical` | Optelling |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedintotal` | Optelling |
| `CustomChannel` | `MyCustomAvailableforReservation` | `fno` | `orderedreserved` | Aftrekken |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `inbound` | Optelling |
| `CustomChannel` | `MyCustomAvailableforReservation` | `mypos` | `outbound` | Aftrekken |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `received` | Optelling |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `scheduled` | Optelling |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `issued` | Aftrekken |
| `CustomChannel` | `MyCustomAvailableforReservation` | `exterchannel` | `reserved` | Aftrekken |

Hiermee retourneert de query voor de aangepaste metingshoeveelheid de volgende uitvoer.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

De `MyCustomAvailableforReservation`-uitvoer is gebaseerd op de berekeningsinstelling in de aangepaste metingen als:  
 *100 + 50 + 80 + 90 + 30 &ndash; 10 &ndash; 20 &ndash; 60 &ndash; 40 = 220*

### <a name="posting-on-hand-changes"></a>Wijzigingen voorhanden voorraad boeken

De exacte URL waarnaar de gebeurtenis wordt geboekt, is afhankelijk van uw geografische regio. Deze heeft de volgende vorm:

`https://{serviceURL}/api/environment/{environmentId}/onhand`

Na verificatie kan deze URL worden gebruikt in combinatie met de HTTP `POST`-methode voor het verzenden van gebeurtenissen voor wijzigingen van de voorhanden voorraad naar de service.

Een speciale header wordt gebruikt voor de communicatie met Dynamics 365-services via HTTP-aanvragen, waarbij de omgevings-ID van het Supply Chain Management-exemplaar wordt aangegeven waaraan de gegevens zijn gekoppeld. Bijvoorbeeld:

`x-ms-environment-id: 2db79622-f97a-4d64-9844-d12efed41796`

#### <a name="posting-on-hand-changes-query-example-1"></a>Queryvoorbeeld 1 voor boeken van wijzigingen voorhanden voorraad

In dit voorbeeld ziet u een scenario waarin u de dimensieconfiguratie in Power Apps kunt instellen.

Met de volgende query configureert u de dimensietoewijzing in Power Apps:

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

U kunt nu de `dimensionDataSource` opgeven en aangepaste dimensies gebruiken in uw query's. Aangepaste dimensies worden automatisch omgezet in basisdimensies.

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensionDataSource": "pos",
    "dimensions": {
        "PosSizeId": "Large",
        "PosColorId": "Red",
        "PosSiteId": "2",
        "PosLocationId": "21"
    }
}
```

#### <a name="posting-on-hand-changes-query-example-2"></a>Queryvoorbeeld 2 voor boeken van wijzigingen voorhanden voorraad

In dit voorbeeld ziet u een scenario waarin er geen toewijzingen zijn ingesteld voor de dimensieconfiguratie in Power Apps. Daarom moet de boeking ook gebruikmaken van de basisdimensies. Alle dimensies moeten basisdimensies zijn als het veld `dimensionDataSource` null, leeg of een spatie is.

```json
{
    "id": "demo-test-00007",
    "organizationId": "usmf",
    "productId": "MyProduct",
    "quantities": {
        "pos": {
            "Outbound": 1
        }
    },
    "dimensions": {
        "SizeId": "Large",
        "ColorId": "Red",
        "SiteId": "2",
        "LocationId": "21"
    }
}
```

#### <a name="json-document-field-properties"></a>JSON-documentveldeigenschappen

De velden uit de eerdere JSON-queryvoorbeelden hebben de eigenschappen die in de volgende tabel worden weergegeven.

| Veld-ID | Beschrijving |
|---|---|
| `id` | Een unieke ID voor de specifieke wijzigingsgebeurtenis. Deze ID wordt gebruikt om ervoor te zorgen dat als bij het boeken de communicatie met de service mislukt, het opnieuw indienen van de gebeurtenis niet ertoe leidt dat dezelfde gebeurtenis tweemaal in het systeem wordt geteld. |
| `organizationId` | De id van de organisatie die aan de gebeurtenis is gekoppeld. Deze is toegewezen aan Supply Chain Management-organisaties of -gegevensgebied-id's. |
| `productId` | De id van het betreffende product. |
| `quantity` | De hoeveelheid waarmee de voorhanden voorraad moet worden gewijzigd. Als er bijvoorbeeld 10 nieuwe bagels aan een plank zijn toegevoegd, is deze waarde 10. Als 3 bagels van de plank worden verwijderd of verkocht, zou deze waarde -3 zijn. |
| `dimensionDataSource` | De gegevensbron van de dimensies gebruikt bij het boeken van de wijzigingsgebeurtenis en query. Als u de gegevensbron opgeeft, kunt u de aangepaste dimensies gebruiken van de opgegeven gegevensbron. Met de dimensieconfiguratie kan Voorraadzichtbaarheid de aangepaste dimensies toewijzen aan de algemene standaarddimensies. Als de `dimensionDataSource` niet is opgegeven, kunt u alleen de algemene standaarddimensies in uw query's gebruiken.   |
| `dimensions` | Een dynamische verzameling sleutel-waardeparen. Deze worden toegewezen aan enkele dimensies in Supply Chain Management, maar u kunt ook aangepaste dimensies (zoals *Bron*) toevoegen die aangeven of de gebeurtenis afkomstig is van Supply Chain Management of een extern systeem. |

### <a name="querying-current-on-hand"></a>Query uitvoeren voor huidige voorhanden voorraad

Het eindpunt voor het uitvoeren van query's voor de huidige voorhanden voorraad heeft een vergelijkbare URL:

`https://{serviceURL}/api/environment/{environmentId}/onhand/indexquery`

Hiervoor worden query's uitgevoerd met de HTTP `POST`-methode.

#### <a name="current-on-hand-query-example-1"></a>Queryvoorbeeld 1 huidige voorhanden voorraad

In dit voorbeeld ziet u een scenario waarin u de dimensieconfiguratie al hebt voltooid in Power Apps.

Met de volgende query configureert u de dimensietoewijzing in Power Apps:

```json
{
    "PosSizeId": "SizeId",
    "PosColorId": "ColorId",
    "PosSiteId": "SiteId",
    "PosLocationId": "LocationId"
}
```

U kunt nu de `dimensionDataSource` opgeven en aangepaste dimensies gebruiken in uw query's. Aangepaste dimensies worden automatisch omgezet in basisdimensies. U kunt de `DimensionDataSource` opgeven in `filters` en aangepaste dimensies opgeven in `filters` en `groupByValues`. Aangepaste dimensies worden automatisch omgezet in basisdimensies.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "DimensionDataSource": ["Pos"],
        "PosLocationId": ["21"],
        "PosSiteId": ["2"],
        "PosColorId": ["Red"]
    },
    "groupByValues": [
        "PosSizeId",
        "PosColorId"
    ],
    "returnNegative": true
}
```

#### <a name="current-on-hand-query-example-2"></a>Queryvoorbeeld 2 huidige voorhanden voorraad

In dit voorbeeld ziet u een scenario waarin er geen toewijzingen zijn ingesteld voor de dimensieconfiguratie in Power Apps. Daarom moet de boeking ook gebruikmaken van de basisdimensies. Alle dimensies moeten basisdimensies zijn als het veld `dimensionDataSource` onder `filters` null, leeg of een spatie is.

```json
{
    "filters": {
        "OrganizationId": ["usmf"],
        "ProductId": ["MyProduct"],
        "LocationId": ["21"],
        "SiteId": ["2"],
        "ColorId": ["Red"]
    },
    "groupByValues": [
        "SizeId",
        "ColorId"
    ],
    "returnNegative": true
}
```

#### <a name="example-return-result"></a>Voorbeeldretourresultaat

De query's die in de vorige voorbeelden worden weergegeven, kunnen een resultaat als dit retourneren.

```json
[
    {
        "productId": "MyProduct",
        "dimensions": {
            "colorid": "Red"
        },
        "quantities": {
            "mypos": {
                "outbound": 20.0,
                "inbound": 80.0
            },
            "fno": {
                "availphysical": 100.0,
                "orderedintotal": 50.0,
                "orderedreserved": 10.0
            },
            "exterchannel": {
                "received": 90.0,
                "scheduled": 30.0,
                "issued": 60.0,
                "reserved": 40.0
            },
            "CustomChannel": {
                "MyCustomAvailableforReservation": 220.0
            }
        }
    }
]
```

De velden met hoeveelheden zijn gestructureerd als een woordenboek met metingen en de bijbehorende waarden.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
