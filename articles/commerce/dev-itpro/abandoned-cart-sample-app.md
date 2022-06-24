---
title: Achtergelaten winkelwagens detecteren en meldingen verzenden naar klanten
description: In dit artikel wordt beschreven hoe u de connectorvoorbeeld-app van Microsoft Dynamics 365 Commerce voor verlaten winkelwagens kunt aanpassen om verlaten winkelwagentjes te detecteren en meldingen per e-mail naar klanten te verzenden.
author: bicyclingfool
ms.date: 02/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 707640ca211e997533d0f5a0b4e6d52cb5be9db4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899205"
---
# <a name="detect-abandoned-carts-and-send-notifications-to-customers"></a>Achtergelaten winkelwagens detecteren en meldingen verzenden naar klanten

[!include [banner](../includes/banner.md)]

In dit artikel wordt beschreven hoe u de connectorvoorbeeld-app van Microsoft Dynamics 365 Commerce voor verlaten winkelwagens kunt aanpassen om verlaten winkelwagentjes te detecteren en meldingen per e-mail naar klanten te verzenden.

De mogelijkheid om opbrengsten te herstellen en klanten te behouden via meldingen over verlaten winkelwagens, is een belangrijke mogelijkheid die door Dynamics 365 Commerce wordt ondersteund. Door de connectorvoorbeeld-app van Commerce voor verlaten winkelwagens aan te passen hebben detailhandelaren toegang tot winkelwagens op Retail Server die gedurende een tijdvenster dat door de detailhandelaren wordt gedefinieerd, niet zijn gewijzigd. Deze winkelwagens kunnen vervolgens samen met product- en klantgegevens worden opgehaald en worden doorgegeven aan een e-mailmarketingprovider van derden die e-mailmeldingen genereert en aan deze klanten verzendt.

Het e-mailbericht over de verlaten winkelwagen dat klanten ontvangen, kan de volgende informatie bevatten:

- De voornaam van de klant.
- De achternaam van de klant.
- Het e-mailadres van de klant.
- Een URL waarmee de klant terugkeert naar de winkelwagen.
- De transactievaluta.
- Een lijst met producten in het winkelwagentje van de klant. Voor elk product is de volgende informatie opgenomen:

    - De weergavenaam van het product
    - De product-id (wordt gebruikt voor een URL naar de pagina met de productomschrijving)
    - Een productafbeelding die automatisch kan worden aangepast aan verschillende viewportafmetingen
    - Alle tekst voor de productafbeelding
    - De eenheidsprijs van het product

## <a name="abandoned-cart-connector-sample"></a>Connectorvoorbeeld van verlaten winkelwagen

Met een connectormodel dat Microsoft levert via de Retail-SDK kunnen gegevens van verlaten winkelwagens worden opgehaald en verzonden naar een e-mailmarketingprovider van een derde partij. Deze connector verwerkt de communicatie met Retail Server, gebruikt hiervoor Azure Key Vault ter beveiliging, verwerkt de planning van het ophalen van winkelwagens voor een opgegeven tijdvenster en haalt order- en productgegevens op. Het biedt ook een voorbeelduitvoering voor een integratie met een e-mailmarketingprovider van een derde partij. De connector is ontworpen om standaard [met Emarsys](https://emarsys.com) te communiceren. U kunt de connector eenvoudig integreren met andere oplossingen, zoals Constant Contact, Mailchimp en SendGrid.

In de volgende afbeelding ziet u de onderdelen van de connectorvoorbeeld-app voor verlaten winkelwagens.

![Onderdelen van de connectorvoorbeeld-app voor verlaten winkelwagens](media/AbandonedCartConnector.png)

> [!IMPORTANT]
> In sommige regio's moeten klanten kunnen instellen dat hun winkelwagengegevens niet worden verzonden naar een e-mailmarketingprovider of kunnen verzoeken om hun gegevens te verwijderen. Deze opties levert Microsoft echter niet voor klanten. Als u van plan bent om zaken te doen in regio's die dit verplicht stellen, moet u de vereiste infrastructuur en aanpassingen leveren om de voorkeuren van klanten bij te houden en desgewenst voorkomen dat klantgegevens worden doorgegeven aan uw e-mailplatform. U moet ook op verzoek van de klant een proces definiëren voor het opschonen van klantgegevens van uw e-mailmarketingprovider.

## <a name="obtain-the-code-sample"></a>Het codevoorbeeld ophalen

De connectorvoorbeeld-app voor verlaten winkelwagens wordt vanaf versie 10.0.16 opgenomen in de Retail SDK. U vindt de code onder **\\RetailSDK\\Code\\SampleExtensions\\RetailServer\\Extensions.AbandonedCartSample**. Zie voor informatie over de Retail-SDK [Retail-SDK (Software Development Kit)](retail-sdk/retail-sdk-overview.md).

> [!NOTE]
> Hoewel de voorbeeldcode voor het eerst beschikbaar was in builds van versie 10.0.16, is deze compatibel met versie 10.0.13 en latere builds van Retail Server.

## <a name="prerequisites-and-dependencies"></a>Vereisten en afhankelijkheden

Voordat u de connectorvoorbeeld-app voor verlaten winkelwagens kunt implementeren en configureren, moet aan de volgende vereisten zijn voldaan.

### <a name="access-to-commerce-resources"></a>Toegang tot Commerce-resources

Voor het configureren en implementeren van de connector-app voor verlaten winkelwagens moet u toegang hebben tot de volgende Commerce-resources:

- Beheerderstoegang tot Commerce Headquarters voor uw omgeving
- Toegang tot het Microsoft Dynamics Lifecycle Services (LCS)-project voor uw omgeving

### <a name="azure-cosmos-db"></a>Azure Cosmos DB

De connectorvoorbeeld-app voor verlaten winkelwagens gebruikt Azure Cosmos DB om de id's en tijdstempels te volgen van winkelwagens die eerder zijn opgehaald. U kunt Azure Cosmos DB gebruiken om deze gegevens toe te passen of u kunt het codevoorbeeld aanpassen om met een andere optie voor gegevensopslag te integreren. Zie [Welkom bij Azure Cosmos DB](/azure/cosmos-db/introduction) voor meer informatie over Azure Cosmos DB.

Als u Azure Cosmos DB gebruikt, moet aan de volgende vereisten zijn voldaan voordat u het voorbeeld kunt uitvoeren:

- U moet over een actief Azure Cosmos DB-account beschikken. Zie [Een databaseaccount maken](/azure/cosmos-db/create-sql-api-dotnet#create-a-database-account) als u geen account hebt.
- U moet de waarden **URI** en **PRIMARY KEY** (of **SECONDARY KEY**) ophalen van het blad **Keys** van uw Azure Cosmos DB-account in de Azure-portal. Zie voor meer informatie over het ophalen van eindpunt- en sleutelgegevens voor uw Azure Cosmos DB-account [Toegangstoetsen en wachtwoorden weergeven, kopiëren en opnieuw genereren](/azure/cosmos-db/manage-account#keys).

### <a name="azure-key-vault"></a>Azure Key Vault

In de connector-app voor verlaten winkelwagens wordt Key Vault gebruikt voor het opslaan van de namen en onderdelen van de verschillende onderdelen die beveiligde toegang vereisen.

Ga als volgt te werk om een sleutelkluis in te stellen.

1. Volg de instructies in [Key Vault in Azure Stack Hub beheren met de portal](/azure-stack/user/azure-stack-key-vault-manage-portal?view=azs-2002&preserve-view=true).
2. U kunt geheimen maken voor de volgende informatie:

    - De gebruikersnaam en API-geheim van de Emarsys-API
    - Toepassings-id en geheim van verlaten winkelwagen

De connectorvoorbeeldcode voor verlaten winkelwagens gebruikt standaardreferenties van Azure om toegang te krijgen tot Key Vault. U moet **lijst-** en **leesmachtigingen** verlenen voor de identiteit die u wilt gebruiken voor de toegang tot Key Vault.

Zie [DefaultAzureCredential Class](/dotnet/api/azure.identity.defaultazurecredential?view=azure-dotnet&preserve-view=true) voor meer informatie over standaardreferenties voor Azure.

## <a name="create-an-abandoned-cart-connector-sample-app-application-id-for-the-azure-ad-tenant"></a>Een toepassings-id voor de connectorvoorbeeld-app van verlaten winkelwagens maken voor de Azure AD-tenant

U moet een toepassings-id voor de connectorvoorbeeld-app van verlaten winkelwagens maken voor de Azure Active Directory-tenant (AD) Zie [De portal gebruiken om een Azure AD-toepassings-id en serviceprincipal te maken die toegang heeft tot resources](/azure/active-directory/develop/howto-create-service-principal-portal) voor meer informatie.

## <a name="add-the-abandoned-cart-connector-sample-app-application-id-to-the-allow-list-for-the-retail-server-api"></a>De toepassings-id voor de connectorvoorbeeld-app voor verlaten winkelwagens toevoegen aan de toegestane lijst voor de Retail Server-API

Vervolgens voegt u de toepassings-id voor de connectorvoorbeeld-app voor verlaten winkelwagens toevoegen aan de toegestane lijst voor de Retail Server-API, Zie [Ondersteuning voor Service-to-Service-verificatie in Retail Server](https://community.dynamics.com/ax/b/axforretail/posts/support-for-service-to-service-authentication-in-retail-server) voor informatie over het toevoegen van een toepassings-id aan de toegestane lijst in Azure.

## <a name="configure-the-abandoned-cart-connector-sample-app"></a>De connectorvoorbeeld-app voor verlaten winkelwagens configureren

Wijzig het configuratiebestand **appSettings.json** in de basis van de map **AbandonedCartDetectionSample** om de connectorvoorbeeld-app voor verlaten winkelwagens te configureren. In de volgende tabellen worden de eigenschappen van het configuratiebestand beschreven.

### <a name="keyvaultoptions"></a>KeyVaultOptions

| Eigenschap    | Description |
| ----------- | ----------- |
| KeyVaultURI | De DNS-naam (Domain Name System) van de belangrijkste sleutelkluisd ie u gebruikt in Azure Portal. |

### <a name="retailserverclientoptions"></a>RetailServerClientOptions

| Eigenschap                                      | Description |
| --------------------------------------------- | ----------- |
| TenantId                                      | De Azure AD-tenant-id van uw Azure-tenant. |
| RetailServerAudienceId                        | De doelgroep-id voor Retail Server. U kunt de standaardwaarde gebruiken. |
| AppIdKeyVaultSecretName                       | De naam van het geheim dat u hebt gemaakt voor de toepassings-id voor de connectorvoorbeeld-app van verlaten winkelwagens. |
| AppSecretKeyVaultSecretName                   | De naam van het geheim waarin het appgeheim voor de toepassings-id voor de connectorvoorbeeld-app van verlaten winkelwagens is opgeslagen. |
| RetailServerUrl                               | De URL van uw Retail Server-exemplaar. Deze waarde vindt u in LCS. |
| OperatingUnitNumber                           | Het nummer van operationele eenheid (OUN). Deze waarde vindt u in Commerce headquarters. |
| IncludeAbandonedCartsModifiedSinceLastMinutes | Het begin van het tijdvenster voor de verlaten winkelwagen die u wilt ophalen. De waarde wordt uitgedrukt als een aantal minuten voor de huidige tijd. Stel deze eigenschap bijvoorbeeld in op **120** om alle winkelwagens op te halen die het laatst zijn gewijzigd tussen 120 minuten geleden en het einde van het tijdvenster dat is gedefinieerd met de eigenschap **ExcludeAbandonedCartsModifiedSinceLastMinutes**. |
| ExcludeAbandonedCartsModifiedSinceLastMinutes | Het einde van het tijdvenster voor de verlaten winkelwagen die u wilt ophalen. De waarde wordt uitgedrukt als een aantal minuten voor de huidige tijd. Als de eigenschap **IncludeAbandonedCartsModifiedSinceLastMinutes** bijvoorbeeld is ingesteld op **120**, stelt u deze eigenschap in op **30** om alle winkelwagentjes op te halen die tussen 120 en 30 minuten geleden zijn gewijzigd. In de praktijk bepaalt deze eigenschap de hoeveelheid tijd die u wilt wachten voordat een winkelwagen als verlaten wordt gezien. |
| ReturnToCartUrl                               | De URL van de winkelwagen op uw e-commercesite, in de indeling die in het bestand **app.config** wordt gebruikt. |

### <a name="azurecosmosoptions"></a>AzureCosmosOptions

De taakstatus, winkelwagen-id's en gewijzigde tijdstempels worden opgeslagen in Azure Cosmos DB. Standaard wijzen de instellingen in het configuratiebestand naar het lokale emulatorexemplaar van Azure Cosmos DB. Wanneer u de connector implementeert naar de productie, moet u deze instellingen bijwerken zodat ze naar het Azure Cosmos DB-exemplaar in uw abonnement Azure wijzen. Voor lokale of sandbox testen gebruikt u de [Azure Cosmos DB Emulator](/azure/cosmos-db/local-emulator).

| Eigenschap    | Description |
| ----------- | ----------- |
| EndPointUri | De eindpunt-URI die wordt geleverd door Azure of de emulator. |
| PrimaryKey  | De primaire sleutel die wordt geleverd door Azure of de emulator. |
| DatabaseId  | De database-id. U kunt de standaardwaarde laten staan of uw eigen waarde opgeven. |
| ContainerId | De container-id. U kunt de standaardwaarde laten staan of uw eigen waarde opgeven. |

### <a name="emarsysclientoptions"></a>EmarsysClientOptions

> [!NOTE]
> Als u integreert met een andere e-mailmarketingprovider dan Emarsys, moet u de **IEmailProvider**-interface zo nodig uitbreiden om met die provider te communiceren.

| Eigenschap                      | Description |
| ----------------------------- | ----------- |
| ApiUrl                        | `https://api.emarsys.net/api/v2/event/{0}/trigger` |
| ExternalEventId               | De id van de externe gebeurtenisrecord die is gemaakt in Emarsys. U vindt de waarde onder **Triggerinstellingen** in de campagne die u hebt gemaakt om e-mailmeldingen over verlaten winkelwagens te verzenden. |
| ApiUserNameKeyVaultSecretName | De naam van de sleutel waar de gebruikersnaam van Emarsys-API is opgeslagen. |
| ApiSecretKeyVaultSecretName   | De naam van de sleutel waar het geheim van Emarsys-API is opgeslagen. |
| EmarsysContactKeyId           | De id van de e-mailkolom in de Emarsys-contactdatabase. De standaardwaarde is **3** en mag niet worden gewijzigd. |

### <a name="mediaoptions"></a>MediaOptions

Als u de e-commercemogelijkheden in Commerce gebruikt, kunt u digitale activabeheer van Commerce gebruiken om afbeeldingen van producten op te halen. Zie [Configuratie van de ImageSettings-viewport](../e-commerce-extensibility/image-component.md#imagesettings-viewport-configuration) voor meer informatie over de mogelijkheden voor Image Resizer in digitaal activabeheer.

| Eigenschap                             | Description |
| ------------------------------------ | ----------- |
| ImageServerUrl                       | De basis-URL van digitaal activabeheer van uw site. U vindt de waarde in de eigenschapsleutel **Basis-URL voor mediaserver** in **Retail en Commerce \> Afzetkanaalinstellingen \> Afzetkanaalprofielen** in Commerce Headquarters. |
| ImageViewPorts                       | Het containerknooppunt voor afzonderlijke viewportconfiguraties. |
| ImageViewPorts/viewport              | De viewportdefinitie Gebruik deze eigenschap om de breedtebereiken voor de viewport op te geven, in pixels. Zie het configuratiebestand **appSettings.json** voor een voorbeeld van het gebruik van deze eigenschap. |
| ImageViewPorts/imageWidth            | De afbeeldingsbreedte van de viewport, in pixels. |
| imageViewPorts/imageHeight           | De afbeeldingshoogte van de viewport, in pixels. |
| imageViewPorts/useForDefaultImageTag | Een waarde **true**/**false** waarmee wordt aangegeven of de afbeeldingsafmetingen van de viewport moeten worden gebruikt als de HTML-code `<picture>` niet wordt ondersteund voor een webbrowser of e-mailclient. |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
