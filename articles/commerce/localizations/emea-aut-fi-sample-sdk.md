---
title: Implementatierichtlijnen voor het voorbeeld van integratie van fiscale registratieservice voor Oostenrijk (verouderd)
description: Dit artikel bevat richtlijnen voor de implementatie van het voorbeeld voor fiscale integratie voor Oostenrijk vanuit de Retail SDK (Software Development Kit) voor Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 03/04/2022
ms.topic: article
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: 94fe6817358ae18126a30794fd52fe5eb01a5265
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885432"
---
# <a name="deployment-guidelines-for-the-fiscal-registration-service-integration-sample-for-austria-legacy"></a>Implementatierichtlijnen voor het voorbeeld van integratie van fiscale registratieservice voor Oostenrijk (verouderd)

[!include [banner](../includes/banner.md)]

Dit artikel bevat richtlijnen voor de implementatie van het voorbeeld voor integratie van de fiscale registratieservice voor Oostenrijk vanuit de Retail Software Development Kit (SDK) van Microsoft Dynamics 365 Commerce op een virtuele machine (VM) voor een developer in Microsoft Dynamics Lifecycle Services (LCS). Zie [Voorbeeld van integratie van fiscale registratieservice voor Oostenrijk](emea-aut-fi-sample.md) voor meer informatie over dit voorbeeld van fiscale integratie. 

Het voorbeeld van fiscale integratie voor Oostenrijk maakt deel uit van de Retail SDK. Zie [Architectuur van Retail SDK (Software Development Kit)](../dev-itpro/retail-sdk/retail-sdk-overview.md) voor informatie over het installeren en gebruiken van de SDK. Het voorbeeld voor fiscale integratie bestaat uit extensies voor Commerce runtime (CRT), hardwarestation en verkooppunt (POS). Als u dit voorbeeld wilt uitvoeren, moet u CRT, hardwarestation en POS-projecten wijzigen en bouwen. Het is raadzaam een niet-geverifieerde Retail SDK te gebruiken om de wijzigingen aan te brengen die in dit artikel worden beschreven. Het wordt ook aangeraden een broncontrolesysteem te gebruiken, zoals Azure DevOps wanneer er nog geen bestanden zijn gewijzigd.

## <a name="development-environment"></a>Ontwikkelingsomgeving

Voer de volgende stappen uit om een ontwikkelingsomgeving in te stellen zodat u het voorbeeld kunt testen en uitbreiden.

### <a name="enable-commerce-runtime-extensions"></a>Commerce Runtime-extensies inschakelen

De CRT-extensieonderdelen zijn opgenomen in de CRT-voorbeelden. Als u de volgende procedures wilt uitvoeren, opent u de oplossing **CommerceRuntimeSamples.sln** onder **RetailSdk\\SampleExtensions\\CommerceRuntime**.

#### <a name="documentproviderefrsample-component"></a>Onderdeel DocumentProvider.EFRSample

1. Zoek het project **Runtime.Extensions.DocumentProvider.EFRSample** en bouw het.
2. Zoek in de map **Runtime.Extensions.DocumentProvider.EFRSample\\bin\\Debug** het assemblagebestand **Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll**.
3. Kopieer het assemblagebestand naar de map met CRT-extensies:

    - **Schaaleenheid commerce**: kopieer het bestand naar de map **\\bin\\ext** onder de locatie van de commerce scale unit van Internet Information Services (IIS).
    - **Lokale CRT op Modern POS:** kopieer het bestand naar de map **\\ext** onder de locatie van de lokale CRT-clientbroker.

4. Zoek het extensieconfiguratiebestand voor CRT:

    - **Commerce Scale Unit:** het bestand heeft de naam **commerceruntime.ext.config** en bevindt zich in de map **bin\\ext** onder de locatie van de Commerce Scale Unit van Internet Information Services (IIS).
    - **Lokaal CRT op Modern POS:** het bestand heeft de naam **CommerceRuntime.MPOSOffline.Ext.config** en bevindt zich onder de locatie van de lokale CRT-clientbroker.

5. Registreer de CRT-wijziging in het extensieconfiguratiebestand.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
    ```

#### <a name="documentproviderdatamodelefr-component"></a>Onderdeel DocumentProvider.DataModelEFR

1. Zoek het project **Runtime.Extensions.DocumentProvider.DataModelEFR** en bouw het.
2. Zoek in de map **Runtime.Extensions.DocumentProvider.DataModelEFR\\bin\\Debug** het assemblagebestand **Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll**.
3. Kopieer het assemblagebestand naar de map met CRT-extensies:

    - **Commerce Scale Unit:** kopieer het bestand naar de map **\\bin\\ext** onder de locatie van de Commerce Scale Unit van Internet Information Services (IIS).
    - **Lokale CRT op Modern POS:** kopieer het bestand naar de map **\\ext** onder de locatie van de lokale CRT-clientbroker.

4. Zoek het extensieconfiguratiebestand voor CRT:

    - **Commerce Scale Unit:** het bestand heeft de naam **commerceruntime.ext.config** en bevindt zich in de map **bin\\ext** onder de locatie van de Commerce Scale Unit van Internet Information Services (IIS).
    - **Lokaal CRT op Modern POS:** het bestand heeft de naam **CommerceRuntime.MPOSOffline.Ext.config** en bevindt zich onder de locatie van de lokale CRT-clientbroker.

5. Registreer de CRT-wijziging in het extensieconfiguratiebestand.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
    ```

#### <a name="extension-configuration-file"></a>Bestand voor extensieconfiguratie

1. Zoek het extensieconfiguratiebestand voor CRT:

    - **Commerce Scale Unit:** het bestand heeft de naam **commerceruntime.ext.config** en bevindt zich in de map **bin\\ext** onder de locatie van de Commerce Scale Unit van Internet Information Services (IIS).
    - **Lokaal CRT op Modern POS:** het bestand heeft de naam **CommerceRuntime.MPOSOffline.Ext.config** en bevindt zich onder de locatie van de lokale CRT-clientbroker.

2. Registreer de CRT-wijziging in het extensieconfiguratiebestand.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsAustria" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventAustria" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.XZReportsAustria" />
    ```

### <a name="enable-fiscal-connector-extensions"></a>Uitbreidingen voor Fiscale connector inschakelen

U kunt uitbreidingen voor de fiscale connector inschakelen op het [hardwarestation](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station) of de [POS-kassa](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-or-service-in-the-local-network).

#### <a name="enable-hardware-station-extensions"></a>Extensies van hardwarestation inschakelen

De onderdelen van de hardwarestationextensie zijn opgenomen in de voorbeelden voor hardwarestation. Als u de volgende procedures wilt uitvoeren, opent u de oplossing **HardwareStationSamples.sln** onder **RetailSdk\\SampleExtensions\\HardwareStation**.

##### <a name="efrsample-component"></a>Onderdeel EFRSample

1. Zoek het project **HardwareStation.Extension.EFRSample** en bouw het.
2. Zoek de volgende assemblagebestanden in de map **Extension.EFRSample\\bin\\Debug**:

    - Contoso.Commerce.HardwareStation.EFRSample.dll
    - Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll

3. Kopieer de assemblagebestanden naar de map met extensies voor het hardwarestation:

    - **Gedeeld hardwarestation**: kopieer de bestanden naar de map **bin** onder de locatie van de IIS-hardwarestationsite.
    - **Speciaal hardwarestation op het Modern POS**: kopieer de bestanden naar de brokerlocatie van de Modern POS-client.

4. Zoek het extensieconfiguratiebestand voor de extensies van het hardwarestation. Het bestand heeft de naam **HardwareStation.Extension.config**.

    - **Gedeeld hardwarestation:** het bestand bevindt zich onder de locatie van de IIS-hardwarestationsite.
    - **Speciaal hardwarestation op het Modern POS**: het bestand bevindt zich onder de brokerlocatie van de Modern POS-client.

5. Voeg de volgende regel toe aan de sectie **samenstelling** van het configuratiebestand.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample.dll" />
    ```

#### <a name="enable-pos-extensions"></a>POS-extensies inschakelen

Het voorbeeld voor de POS-extensie bevindt zich in de map **src\\FiscalIntegration\\PosFiscalConnectorSample** van de opslagplaats [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/).

Voer de volgende stappen uit om het POS-extensievoorbeeld uit de oude SDK te gebruiken.

1. Kopieer de map **Pos.Extension** naar de map POS **Extensies** van de verouderde SDK (bijvoorbeeld `C:\RetailSDK\src\POS\Extensions`)
1. Wijzig de naam van de kopie van de map **Pos.Extension** **PosFiscalConnector**.
1. Verwijder de volgende mappen en bestanden uit de map **PosFiscalConnector**:

    - bin
    - DataService
    - devDependencies
    - Bibliotheken
    - obj
    - Contoso.PosFiscalConnectorSample.Pos.csproj
    - RetailServerEdmxModel.g.xml
    - tsconfig.json

1. Open de oplossing **CloudPos.sln** of **ModernPos.sln**.
1. Neem in het project **Pos.Extensions** de map **PosFiscalConnector** op.
1. Open het bestand **extensions.json** en voeg de extensie **PosFiscalConnector** toe.
1. Maak de SDK.

### <a name="enable-modern-pos-extension-components"></a>Onderdelen van Modern POS-extensies inschakelen

1. Open de oplossing **ModernPOS.sln** onder **RetailSdk\\POS** en zorg ervoor dat deze zonder fouten kan worden gecompileerd. Zorg er bovendien voor dat u Modern POS kunt uitvoeren vanuit Visual Studio met de opdracht **Uitvoeren**.

    > [!NOTE]
    > Modern POS mag niet worden aangepast. U moet User Account Control (UAC) inschakelen en u moet de installatie van eerder geïnstalleerde exemplaren van Modern POS zo nodig ongedaan maken.

2. Schakel de extensies in die moeten worden geladen door de volgende regels toe te voegen aan het bestand **extensions.json**.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.AT"
            }
        ]
    }
    ```

    > [!NOTE]
    > Zie de instructies in het bestand readme.md in het project **Pos.Extensions** voor meer informatie en voorbeelden over het opnemen van mappen met broncodes en het inschakelen van te laden extensies.

3. Bouw de oplossing opnieuw.
4. Voer Modern POS in de debugger uit en test de functionaliteit.

### <a name="enable-cloud-pos-extension-components"></a>Onderdelen van Cloud POS-extensies inschakelen

1. Open de oplossing **CloudPOS.sln** onder **RetailSdk\\POS** en zorg ervoor dat deze zonder fouten kan worden gecompileerd.
2. Schakel de extensies in die moeten worden geladen door de volgende regels toe te voegen aan het bestand **extensions.json**.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.AT"
            }
        ]
    }
    ```

    > [!NOTE]
    > Zie de instructies in het bestand readme.md in het project **Pos.Extensions** voor meer informatie en voorbeelden over het opnemen van mappen met broncodes en het inschakelen van te laden extensies.

3. Bouw de oplossing opnieuw.
4. Voer de oplossing uit met de opdracht **Uitvoeren** en volg de stappen in de handleiding voor de Retail SDK.

## <a name="production-environment"></a>Productieomgeving

De vorige procedure maakt de extensies die onderdelen zijn van het voorbeeld van integratie van fiscale registratieservice mogelijk. Daarnaast moet u deze stappen volgen om implementeerbare pakketten te maken die Commerce-onderdelen bevatten, en om deze pakketten toe te passen in een productieomgeving.

1. Breng de volgende wijzigingen aan in de pakketconfiguratiebestanden onder de map **RetailSdk\\Assets**:

    - Voeg in de configuratiebestanden **commerceruntime.ext.config** en **CommerceRuntime.MPOSOffline.Ext.config** de volgende regels toe aan de sectie **Samenstelling**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsAustria" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.RegisterAuditEventAustria" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.XZReportsAustria" />
        ```

    - Voeg de volgende regel toe aan de sectie **Samenstelling** van het configuratiebestand **HardwareStation.Extension.config**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EFRSample" />
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR" />
        ```

2. Breng de volgende wijzigingen aan in het configuratiebestand voor pakketaanpassing **Customization.settings** onder de map **BuildTools**:

    - Voeg de volgende regels toe om de CRT-extensies op te nemen in de implementeerbare pakketten.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EFRSample.dll" />
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

    - Voeg de volgende regel toe om de extensie voor hardwarestations op te nemen in de implementeerbare pakketten.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EFRSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.DataModelEFR.dll" />
        ```

3. Start de MSBuild-opdrachtprompt voor het hulpprogramma Visual Studio en voer **msbuild** uit onder de map Retail SDK om implementeerbare pakketten te maken.
4. Pas de pakketten toe via LCS of handmatig. Zie [Implementeerbare pakketten maken](../dev-itpro/retail-sdk/retail-sdk-packaging.md) voor meer informatie.
5. Voltooi alle vereiste instellingstaken die worden beschreven in [Commerce instellen voor Oostenrijk](emea-aut-fi-sample.md#set-up-commerce-for-austria).

## <a name="design-of-extensions"></a>Ontwerp van extensies

Het voorbeeld van integratie van fiscale registratieservice voor Oostenrijk is gebaseerd op de [functionaliteit voor fiscale integratie](fiscal-integration-for-retail-channel.md). Zie het [overzicht van het ontwerp van een voorbeeld voor fiscale integratie](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) voor meer informatie over het ontwerp van de oplossing voor fiscale integratie.

### <a name="commerce-runtime-extension-design"></a>Ontwerp van Commerce runtime-extensie

De extensie die een fiscale documentprovider is, heeft tot doel om servicespecifieke documenten te genereren en responsen van de fiscale registratieservice af te handelen.

De CRT-extensie is **Runtime.Extensions.DocumentProvider.EFRSample**.

#### <a name="request-handler"></a>Aanvraaghandler

Er zijn twee aanvraaghandlers voor documentproviders:

- **DocumentProviderEFRFiscalAUT**: deze handler wordt gebruikt om fiscale documenten voor de fiscale registratieservice te genereren.
- **DocumentProviderEFRNonFiscalAUT**: deze handler wordt gebruikt om niet-fiscale documenten voor de fiscale registratieservice te genereren.

Deze handlers worden overgenomen van de interface **INamedRequestHandler**. De methode **HandlerName** is verantwoordelijk voor het retourneren van de naam van de handler. De handlernaam moet overeenkomen met de naam van de connector-documentprovider die is opgegeven in Commerce Headquarters.

De connector ondersteunt de volgende aanvragen:

- **GetFiscalDocumentDocumentProviderRequest**: deze aanvraag bevat informatie over welk document moet worden gegenereerd. Het retourneert een servicespecifieke document dat in de fiscale registratieservice moet worden geregistreerd.
- **GetNonFiscalDocumentDocumentProviderRequest**: deze aanvraag bevat informatie over welk niet-fiscaal document moet worden gegenereerd. Het retourneert een servicespecifieke document dat in de fiscale registratieservice moet worden geregistreerd.
- **GetSupportedRegistrableEventsDocumentProviderRequest**: met deze aanvraag retourneert u de lijst met gebeurtenissen waarop u een abonnement wilt nemen. Op dit moment worden de volgende gebeurtenissen ondersteund: verkoop, afdrukken X-rapport, afdrukken Z-rapport, klantrekeningstortingen, klantorderstortingen, controlegebeurtenissen en niet-verkooptransacties.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest:** met deze aanvraag wordt het antwoord van de fiscale registratieservice geretourneerd. Dit antwoord wordt geseraliseerd om een tekenreeks te vormen zodat deze gereed is om te worden opgeslagen.

#### <a name="configuration"></a>Configuratie

De configuratiebestanden bevinden zich in de map **Configuration** van het extensieproject:

- **DocumentProviderFiscalEFRSampleAustria**: voor fiscale documenten.
- **DocumentProviderNonFiscalEFRSampleAustria**: voor niet-fiscale documenten.

Het doel van deze bestanden is het inschakelen van instellingen die moeten worden geconfigureerd voor de documentprovider vanuit Commerce Headquarters. De bestandsindeling is afgestemd op de vereisten voor de configuratie van fiscale integratie. De volgende instelling wordt toegevoegd:

- Toewijzing van btw-tarieven

### <a name="hardware-station-extension-design"></a>Ontwerp van extensies voor hardwarestation

De fiscale connectorextensie heeft tot doel om te communiceren met de fiscale registratieservice. De extensienaam voor hardwarestations is **HardwareStation.Extension.EFRSample**. Het gebruikt het HTTPS-protocol om documenten die de CRT-extensie genereert in te dienen bij de fiscale registratieservice. Het verwerkt ook de responsen die van de fiscale registratieservice worden ontvangen.

#### <a name="request-handler"></a>Aanvraaghandler

De aanvraaghandler **EFRHandler** is het invoerpunt voor het afhandelen van aanvragen bij de fiscale registratieservice.

De handler wordt overgenomen van de interface **INamedRequestHandler**. De methode **HandlerName** is verantwoordelijk voor het retourneren van de naam van de handler. De handlernaam moet overeenkomen met de naam van de fiscale connector die is opgegeven in Commerce Headquarters.

De connector ondersteunt de volgende aanvragen:

- **SubmitDocumentFiscalDeviceRequest**: met deze aanvraag worden documenten naar de fiscale registratieservice verzonden en wordt hierop een respons geretourneerd.
- **IsReadyFiscalDeviceRequest**: deze aanvraag wordt gebruikt voor een statuscontrole van de fiscale registratieservice.
- **InitializeFiscalDeviceRequest**: deze aanvraag wordt gebruikt om de fiscale registratieservice te initialiseren.

#### <a name="configuration"></a>Configuratie

Het configuratiebestand bevindt zich in de map **Configuration** van het extensieproject. Het doel van het bestand is het inschakelen van instellingen voor de fiscale connector die moet worden geconfigureerd vanuit Commerce Headquarters. De bestandsindeling is afgestemd op de vereisten voor de configuratie van fiscale integratie. De volgende instellingen worden toegevoegd:

- **Eindpuntadres**: de URL van de fiscale registratieservice.
- **Time-out**: de hoeveelheid tijd in milliseconden dat het stuurprogramma wacht op een respons van de fiscale registratieservice.

### <a name="pos-fiscal-connector-extension-design"></a>Uitbreidingsontwerp voor POS fiscale connector

Het doel van de fiscale POS-connectorextensie communiceren met de fiscale registratieservice vanuit POS. Het gebruikt het HTTPS-protocol voor communicatie.

#### <a name="fiscal-connector-factory"></a>Fiscale connectorfactory

De fiscale connectorfactory wordt gekoppeld aan de implementatie van Fiscal Connector en bevindt zich in het bestand **Pos.Extension\\Connectors\\FiscalConnectorFactory.ts**. De connectornaam moet overeenkomen met de naam van de fiscale connector die is opgegeven in Commerce Headquarters.

#### <a name="efr-fiscal-connector"></a>EFR fiscale connector

De EFR-fiscale connector bevindt zich in het bestand **Pos.Extension\\Connectors\\Efr\\EfrFiscalConnector.ts**. Deze implementeert de interface **IFiscalConnector** die de volgende aanvragen ondersteunt:

- **FiscalRegisterSubmitDocumentClientRequest**: met deze aanvraag worden documenten naar de fiscale registratieservice verzonden en wordt hierop een respons geretourneerd.
- **FiscalRegisterIsReadyClientRequest**: deze aanvraag wordt gebruikt voor een statuscontrole van de fiscale registratieservice.
- **FiscalRegisterInitializeClientRequest**: deze aanvraag wordt gebruikt om de fiscale registratieservice te initialiseren.

#### <a name="configuration"></a>Configuratie

Het configuratiebestand bevindt zich in de map **src\\FiscalIntegration\\Efr\\Configurations\\Connectors** van de opslagplaats [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Het doel van het bestand is het inschakelen van instellingen voor de fiscale connector die moet worden geconfigureerd vanuit Commerce Headquarters. De bestandsindeling is afgestemd op de vereisten voor de configuratie van fiscale integratie. De volgende instellingen worden toegevoegd:

- **Eindpuntadres**: de URL van de fiscale registratieservice.
- **Time-out**: de hoeveelheid tijd in milliseconden dat de connector wacht op een respons van de fiscale registratieservice.
