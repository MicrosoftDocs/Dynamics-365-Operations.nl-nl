---
title: Implementatierichtlijnen voor het voorbeeld voor integratie van regeleenheden voor Zweden (verouderd)
description: Dit onderwerp bevat richtlijnen voor de implementatie van het voorbeeld voor integratie van regeleenheden voor Zweden vanuit de Retail SDK
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: b8d60f32d986dec6bb26d78ebdfe8cee3a6b688a
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2022
ms.locfileid: "8077033"
---
# <a name="deployment-guidelines-for-the-control-unit-integration-sample-for-sweden-legacy"></a>Implementatierichtlijnen voor het voorbeeld voor integratie van regeleenheden voor Zweden (verouderd)

[!include [banner](../includes/banner.md)]

Dit onderwerp bevat richtlijnen voor de implementatie van het voorbeeld voor integratie van regeleenheden voor Zweden vanuit de Retail Software Development Kit (SDK) op een virtuele machine (VM) voor een developer in Microsoft Dynamics Lifecycle Services (LCS). Zie [Voorbeeld van integratie van regeleenheid voor Zweden](emea-swe-fi-sample.md) voor meer informatie over dit voorbeeld van fiscale integratie. 

Het voorbeeld van fiscale integratie voor Zweden maakt deel uit van de Retail SDK. Zie [Architectuur van Retail SDK (Software Development Kit)](../dev-itpro/retail-sdk/retail-sdk-overview.md) voor informatie over het installeren en gebruiken van de SDK. Dit voorbeeld bestaat uit extensies voor Commerce runtime (CRT), hardwarestation en verkooppunt (POS). Als u dit voorbeeld wilt uitvoeren, moet u CRT, hardwarestation en POS-projecten wijzigen en bouwen. Het is raadzaam een niet-geverifieerde Retail SDK te gebruiken om de wijzigingen aan te brengen die in dit onderwerp worden beschreven. Het wordt ook aangeraden een broncontrolesysteem te gebruiken, zoals Azure DevOps wanneer er nog geen bestanden zijn gewijzigd.

## <a name="development-environment"></a>Ontwikkelingsomgeving

Voer de volgende stappen uit om een ontwikkelingsomgeving in te stellen zodat u het voorbeeld kunt testen en uitbreiden.

### <a name="enable-crt-extensions"></a>CRT-extensies inschakelen

De CRT-extensieonderdelen zijn opgenomen in de CRT-voorbeelden. Als u de volgende procedures wilt uitvoeren, opent u de oplossing **CommerceRuntimeSamples.sln** onder **RetailSdk\\SampleExtensions\\CommerceRuntime**.

#### <a name="documentprovidercleancashsample-component"></a>Onderdeel DocumentProvider.CleanCashSample

1. Zoek het project **Runtime.Extensions.DocumentProvider.CleanCashSample** en bouw het.
2. Zoek in de map **Runtime.Extensions.DocumentProvider.CleanCashSample\\bin\\Debug** het assemblagebestand **Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll**.
3. Kopieer het assemblagebestand naar de map met CRT-extensies:

    - **Schaaleenheid commerce**: kopieer het bestand naar de map **\\bin\\ext** onder de locatie van de commerce scale unit van Internet Information Services (IIS).
    - **Lokale CRT op Modern POS:** kopieer het bestand naar de map **\\ext** onder de locatie van de lokale CRT-clientbroker.

4. Zoek het extensieconfiguratiebestand voor CRT:

    - **Commerce Scale Unit:** het bestand heeft de naam **commerceruntime.ext.config** en bevindt zich in de map **bin\\ext** onder de locatie van de Commerce Scale Unit van Internet Information Services (IIS).
    - **Lokaal CRT op Modern POS:** het bestand heeft de naam **CommerceRuntime.MPOSOffline.Ext.config** en bevindt zich onder de locatie van de lokale CRT-clientbroker.

5. Registreer de CRT-wijziging in het extensieconfiguratiebestand.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    ```

#### <a name="extension-configuration-file"></a>Bestand voor extensieconfiguratie

1. Zoek het extensieconfiguratiebestand voor CRT:

    - **Commerce Scale Unit:** het bestand heeft de naam **commerceruntime.ext.config** en bevindt zich in de map **bin\\ext** onder de locatie van de Commerce Scale Unit van Internet Information Services (IIS).
    - **Lokaal CRT op Modern POS:** het bestand heeft de naam **CommerceRuntime.MPOSOffline.Ext.config** en bevindt zich onder de locatie van de lokale CRT-clientbroker.

2. Registreer de CRT-wijziging in het extensieconfiguratiebestand.

    ``` xml
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

### <a name="enable-hardware-station-extensions"></a>Extensies van hardwarestation inschakelen

De onderdelen van de hardwarestationextensie zijn opgenomen in de voorbeelden voor hardwarestation. Als u de volgende procedures wilt uitvoeren, opent u de oplossing **HardwareStationSamples.sln** onder **RetailSdk\\SampleExtensions\\HardwareStation**.

#### <a name="cleancash-component"></a>CleanCash-onderdeel

1. Zoek het project **HardwareStation.Extension.CleanCashSample** en bouw het.
2. Zoek in de map **Extension.CleanCashSample\\bin\\Debug** de assemblagebestanden **Contoso.Commerce.HardwareStation.CleanCashSample.dll** en **Interop.CleanCash\_1\_1.dll**.
3. Kopieer de assemblagebestanden naar de map met extensies voor het hardwarestation:

    - **Gedeeld hardwarestation**: kopieer de bestanden naar de map **bin** onder de locatie van de IIS-hardwarestationsite.
    - **Speciaal hardwarestation op het Modern POS**: kopieer de bestanden naar de brokerlocatie van de Modern POS-client.

4. Zoek het extensieconfiguratiebestand voor de extensies van het hardwarestation. Het bestand heeft de naam **HardwareStation.Extension.config**.

    - **Gedeeld hardwarestation:** het bestand bevindt zich onder de locatie van de IIS-hardwarestationsite.
    - **Speciaal hardwarestation op het Modern POS**: het bestand bevindt zich onder de brokerlocatie van de Modern POS-client.

5. Voeg de volgende regel toe aan de sectie **samenstelling** van het configuratiebestand.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

### <a name="enable-modern-pos-extension-components"></a>Onderdelen van Modern POS-extensies inschakelen

1. Open de oplossing **ModernPOS.sln** onder **RetailSdk\\POS** en zorg ervoor dat deze zonder fouten kan worden gecompileerd. Zorg er bovendien voor dat u Modern POS kunt uitvoeren vanuit Visual Studio met de opdracht **Uitvoeren**.

    > [!NOTE]
    > Modern POS mag niet worden aangepast. U moet User Account Control (UAC) inschakelen en u moet de installatie van eerder geïnstalleerde exemplaren van Modern POS zo nodig ongedaan maken.

2. Schakel de extensies in die moeten worden geladen door de volgende regels toe te voegen aan het bestand **extensions.json**.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
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
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

    > [!NOTE]
    > Zie de instructies in het bestand readme.md in het project **Pos.Extensions** voor meer informatie en voorbeelden over het opnemen van mappen met broncodes en het inschakelen van te laden extensies.

3. Bouw de oplossing opnieuw.
4. Voer de oplossing uit met de opdracht **Uitvoeren** en volg de stappen in de handleiding voor de Retail SDK.

## <a name="production-environment"></a>Productieomgeving

De vorige procedure maakt de extensies die onderdelen zijn van het voorbeeld van integratie van regeleenheden mogelijk. Daarnaast moet u deze stappen volgen om implementeerbare pakketten te maken die Commerce-onderdelen bevatten, en om deze pakketten toe te passen in een productieomgeving.

1. Breng de volgende wijzigingen aan in de pakketconfiguratiebestanden onder de map **RetailSdk\\Assets**:

    - Voeg in de configuratiebestanden **commerceruntime.ext.config** en **CommerceRuntime.MPOSOffline.Ext.config** de volgende regels toe aan de sectie **Samenstelling**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
        <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
        ```

    - Voeg de volgende regel toe aan de sectie **Samenstelling** van het configuratiebestand **HardwareStation.Extension.config**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
        ```

2. Breng de volgende wijzigingen aan in het configuratiebestand voor pakketaanpassing **Customization.settings** onder de map **BuildTools**:

    - Voeg de volgende regel toe om de CRT-extensies op te nemen in de implementeerbare pakketten.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
        ```

    - Voeg de volgende regels toe om de extensie voor hardwarestations op te nemen in de implementeerbare pakketten.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
        ```

3. Schakel de POS-extensie in door de volgende regels toe te voegen aan het bestand **extensions.json** onder de map **RetailSDK\\POS\\Extensions**.

    ``` json
    {
        "extensionPackages": [
            {
            "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

4. Start de MSBuild-opdrachtprompt voor het hulpprogramma Visual Studio en voer **msbuild** uit onder de map Retail SDK om implementeerbare pakketten te maken.
5. Pas de pakketten toe via LCS of handmatig. Zie [Implementeerbare pakketten maken](../dev-itpro/retail-sdk/retail-sdk-packaging.md) voor meer informatie.
6. Voltooi alle vereiste instellingstaken die worden beschreven in [De integratie instellen met regeleenheden](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units).

## <a name="design-of-the-extensions"></a>Ontwerp van de extensies

### <a name="crt-extension-design"></a>Ontwerp van CRT-extensies

De extensie die een fiscale documentprovider is, heeft tot doel om servicespecifieke documenten te genereren en responsen van de regeleenheid af te handelen.

De CRT-extensie is **Runtime.Extensions.DocumentProvider.CleanCashSample**.

Zie [Fiscaal registratieproces en fiscale integratievoorbeelden voor fiscale apparaten en services](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) voor meer informatie over het ontwerp van de oplossing voor fiscale integratie.

#### <a name="request-handler"></a>Aanvraaghandler

Er is een enkele **DocumentProviderCleanCash**-aanvraaghandler voor de documentprovider. Deze handler wordt gebruikt om belastingdocumenten voor de regeleenheid te genereren.

Deze handler wordt overgenomen van de interface **INamedRequestHandler**. De methode **HandlerName** is verantwoordelijk voor het retourneren van de naam van de handler. De handlernaam moet overeenkomen met de naam van de connector-documentprovider die is opgegeven in Commerce Headquarters.

De connector ondersteunt de volgende aanvragen:

- **GetFiscalDocumentDocumentProviderRequest**: deze aanvraag bevat informatie over welk document moet worden gegenereerd. Het retourneert een servicespecifieke document dat in de regeleenheid moet worden geregistreerd.
- **GetSupportedRegistrableEventsDocumentProviderRequest**: met deze aanvraag retourneert u de lijst met gebeurtenissen waarop u een abonnement wilt nemen. Op dit moment worden verkoopgebeurtenissen en auditgebeurtenissen ondersteund.

#### <a name="configuration"></a>Configuratie

Het configuratiebestand **DocumentProviderFiscalCleanCashSample** bevindt zich in de map **Configuration** van het extensieproject. Het doel van dit bestand is het inschakelen van instellingen die moeten worden geconfigureerd voor de documentprovider vanuit Commerce Headquarters. De bestandsindeling is afgestemd op de vereisten voor de configuratie van fiscale integratie. De volgende instellingen worden toegevoegd:

- Toewijzing van btw-codes

### <a name="hardware-station-extension-design"></a>Ontwerp van extensies voor hardwarestation

De extensie die een fiscale connector is, heeft tot doel om te communiceren met de regeleenheid.

De extensie voor hardwarestations is **HardwareStation.Extension.CleanCashSample**. Het gebruikt het HTTP-protocol om documenten die de CRT-extensie genereert in te dienen bij de regeleenheid. Het verwerkt ook de responsen die van de regeleenheid worden ontvangen.

#### <a name="request-handler"></a>Aanvraaghandler

De aanvraaghandler **CleanCashHandler** is het invoerpunt voor het verwerken van aanvragen voor de regeleenheid.

De handler wordt overgenomen van de interface **INamedRequestHandler**. De methode **HandlerName** is verantwoordelijk voor het retourneren van de naam van de handler. De handlernaam moet overeenkomen met de naam van de fiscale connector die is opgegeven in Commerce Headquarters.

De connector ondersteunt de volgende aanvragen:

- **SubmitDocumentFiscalDeviceRequest**: met deze aanvraag worden documenten naar de regeleenheid verzonden en wordt hierop een respons geretourneerd.
- **IsReadyFiscalDeviceRequest**: deze aanvraag wordt gebruikt voor een statuscontrole van de regeleenheid.
- **InitializeFiscalDeviceRequest**: deze aanvraag wordt gebruikt om de regeleenheid te initialiseren.

#### <a name="configuration"></a>Configuratie

Het configuratiebestand staat in de map **Configuration** van het extensieproject. Het doel van het bestand is het inschakelen van instellingen voor de fiscale connector die moet worden geconfigureerd vanuit Commerce Headquarters. De bestandsindeling is afgestemd op de vereisten voor de configuratie van fiscale integratie. De volgende instellingen worden toegevoegd:

- **Verbindingsreeks**: de instellingen van de regeleenheid.
- **Time-out**: de hoeveelheid tijd in milliseconden dat het stuurprogramma wacht op een respons van de regeleenheid.

## <a name="migrating-from-the-earlier-integration-sample"></a>Migreren van de eerdere integratievoorbeeld

Als u het eerdere [voorbeeld voor POS-integratie met regeleenheden voor Zweden](retail-sdk-control-unit-sample.md) gebruikt, moet u mogelijk vanuit dit voorbeeld migreren naar het huidige integratievoorbeeld. Als u de wijziging wilt uitvoeren en in de toekomst tijdige updates wilt ontvangen voor de functies voor Zweden, moet u mogelijk een upgrade uitvoeren, minimale code- en configuratiecorrecties aanbrengen in de extensies die u hebt gemaakt en uw oplossingen opnieuw bouwen. Er zijn geen belangrijke wijzigingen vereist in de extensielogica die u hebt gemaakt. Het eerdere integratievoorbeeld en uw aanpassingen blijven werken als er geen wijzigingen van uw kant zijn aangebracht. Daarom kunt u het uitbreiden van uw omgeving plannen, voorbereiden en uitvoeren.

### <a name="migration-process"></a>Migratieproces

De migratie van het eerdere integratievoorbeeld naar het huidige voorbeeld van de integratie van regeleenheden moet worden gebaseerd op het concept van een geleidelijke update. Met andere woorden, alle onderdelen van Commerce Headquarters en Commerce Scale Unit moeten al zijn bijgewerkt voordat u de onderdelen van POS en hardwarestation gaat bijwerken.

Om een situatie te voorkomen waarin een gebeurtenis of transactie tweemaal wordt ondertekend (dat wil zeggen door zowel het eerdere extensie als de huidige extensie) of waarbij een gebeurtenis of transactie niet kan worden ondertekend vanwege de ontbrekende configuratie, raden we u aan om alle POS- en hardwarestationapparaten die het eerdere voorbeeld gebruiken uit te schakelen en ze vervolgens allemaal tegelijk bij te werken. Deze gelijktijdige update kan bijvoorbeeld worden uitgevoerd per winkel door het functionaliteitsprofiel van de winkel en het hardwareprofiel van het hardwarestation bij te werken.

Het migratieproces moet uit de volgende stappen bestaan.

1. De onderdelen van Commerce Headquarters bijwerken.
1. De onderdelen van de Commerce Scale Unit bijwerken en de extensies van het huidige voorbeeld inschakelen.
1. Ervoor dat alle offline transacties zijn gesynchroniseerd vanuit offline-ingeschakelde MPOS-apparaten.
1. Alle apparaten uitschakelen die de onderdelen van het eerdere voorbeeld gebruiken.
1. Voltooi alle vereiste instellingstaken die worden beschreven in [De integratie instellen met regeleenheden](emea-swe-fi-sample.md#setting-up-the-integration-with-control-units).
1. Werk de onderdelen van het POS- en hardwarestation bij, schakel de extensies die deel uitmaken van het eerdere voorbeeld uit en schakel de extensies van het huidige voorbeeld in.

    > [!NOTE]
    > Afhankelijk van het type omgeving kunt u meer technische details over het migratieproces vinden in de sectie [Migratie in een ontwikkelomgeving](#migration-in-a-development-environment) of de sectie [Migratie in een productieomgeving](#migration-in-a-production-environment) van dit onderwerp.

### <a name="migration-in-a-development-environment"></a>Migratie in een ontwikkelomgeving

#### <a name="update-crt"></a>CRT bijwerken

1. Zoek het project **Runtime.Extensions.DocumentProvider.CleanCashSample** en bouw het.
2. Zoek in de map **Runtime.Extensions.DocumentProvider.CleanCashSample\\bin\\Debug** het assemblagebestand **Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll**.
3. Kopieer het assemblagebestand naar de map met CRT-extensies:

    - **Commerce Scale Unit:** kopieer het bestand naar de map **\\bin\\ext** onder de locatie van de Commerce Scale Unit van Internet Information Services (IIS).
    - **Lokale CRT op Modern POS:** kopieer het bestand naar de map **\\ext** onder de locatie van de lokale CRT-clientbroker.

4. Zoek het extensieconfiguratiebestand voor CRT:

    - **Commerce Scale Unit:** het bestand heeft de naam **CommerceRuntime.ext.config** en bevindt zich in de map **bin\\ext** onder de locatie van de Commerce Scale Unit van Internet Information Services (IIS).
    - **Lokale CRT op Modern POS**: het bestand heeft de naam **CommerceRuntime.MPOSOffline.Ext.config** en bevindt zich in de map **bin\\ext** onder de locatie van de lokale CRT-clientbroker.

    > [!WARNING]
    > Bewerk de bestanden CommerceRuntime.config en CommerceRuntime.MPOSOffline.config **niet**. Deze bestanden zijn niet bedoeld voor aanpassingen.

5. Zoek en verwijder de eerdere CRT-extensie uit het extensieconfiguratiebestand.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
    ```

    > [!WARNING]
    > Voltooi deze stap pas wanneer u alle POS-apparaten bijwerkt die met dit CRT-exemplaar werken.

6. Registreer de huidige CRT-voorbeeldextensies in het extensieconfiguratiebestand door de volgende regels toe te voegen.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

#### <a name="update-hardware-station"></a>Hardwarestations bijwerken

1. Zoek het project **HardwareStation.Extension.CleanCashSample** en bouw het.
2. Zoek in de map **Extension.CleanCashSample\\bin\\Debug** de assemblagebestanden **Contoso.Commerce.HardwareStation.CleanCashSample.dll** en **Interop.CleanCash\_1\_1.dll**.
3. Kopieer de assemblagebestanden naar de map met extensies voor het hardwarestation:

    - **Gedeeld hardwarestation**: kopieer de bestanden naar de map **bin** onder de locatie van de IIS-hardwarestationsite.
    - **Speciaal hardwarestation op het Modern POS**: kopieer de bestanden naar de brokerlocatie van de Modern POS-client.

4. Zoek het extensieconfiguratiebestand **HardwareStation.Extension.config**:

    - **Extern hardwarestation:** het bestand bevindt zich onder de locatie van de IIS-hardwarestationsite.
    - **Lokaal hardwarestation op Modern POS**: het bestand bevindt zich onder de brokerlocatie van de Modern POS-client.

    > [!WARNING]
    > Bewerk de bestanden CommerceRuntime.config en CommerceRuntime.MPOSOffline.config **niet**. Deze bestanden zijn niet bedoeld voor aanpassingen.

5. Zoek en verwijder de eerdere extensie voor hardwarestations uit het extensieconfiguratiebestand.

    # <a name="retail-73-and-earlier"></a>[Retail 7.3 en eerder](#tab/retail-7-3)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-731-and-later"></a>[Retail 7.3.1 en later](#tab/retail-7-3-1)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-100-and-later"></a>[Retail 10.0 en later](#tab/retail-10-0)

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
    ```
    ---

6. Voeg de volgende regel toe aan de sectie **samenstelling** van het extensieconfiguratiebestand.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

#### <a name="update-modern-pos"></a>Modern POS bijwerken

1. Open de oplossing **cloudPOS.sln** onder **RetailSdk\\POS**.
2. Schakel de eerdere POS-extensie uit door de volgende regels te verwijderen uit het bestand **extensions.json**.

    ``` json
    {
        "baseUrl": "FiscalRegisterSample"
    }
    ```

2. Schakel de huidige voorbeeldextensie voor POS in door de volgende regels toe te voegen aan het bestand **extensions.json**.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="update-cloud-pos"></a>Cloud-POS bijwerken

1. Open de oplossing **ModernPOS.sln** onder **RetailSdk\\POS**.
2. Schakel de eerdere POS-extensie uit door de volgende regels te verwijderen uit het bestand **extensions.json**.

    ``` json
    {
        "baseUrl": "FiscalRegisterSample"
    }
    ```

2. Schakel de huidige voorbeeldextensie voor POS in door de volgende regels toe te voegen aan het bestand **extensions.json**.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

### <a name="migration-in-a-production-environment"></a>Migratie in een productieomgeving

#### <a name="update-crt"></a>CRT bijwerken

1. Verwijder de eerdere CRT-extensie uit de configuratiebestanden **CommerceRuntime.ext.config** en **CommerceRuntime.MPOSOffline.Ext.config** onder de map **RetailSdk\\Assets**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.FiscalRegisterReceiptSample" />
    ```

    > [!WARNING]
    > Voltooi deze stap pas wanneer u alle POS-apparaten bijwerkt die met dit CRT-exemplaar werken.

2. Verwijder de huidige CRT-voorbeeldextensies door de volgende wijzigingen uit te voeren in de configuratiebestanden **CommerceRuntime.ext.config** en **CommerceRuntime.MPOSOffline.Ext.config** onder de map **RetailSdk\\Assets**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample" />
    <add source="assembly" value="Microsoft.Dynamics.Commerce.Runtime.ReceiptsSweden" />
    ```

3. Voeg in het configuratiebestand voor pakketaanpassingen **Customization.settings** onder de map **BuildTools** de volgende regel toe om de huidige CRT-voorbeeldextensie op te nemen in implementeerbare pakketten.

    ``` xml
    <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.CleanCashSample.dll" />
    ```

#### <a name="update-hardware-station"></a>Hardwarestations bijwerken

1. Verwijder de eerdere extensie voor hardwarestations door het configuratiebestand **HardwareStation.Extension.config** te wijzigen.

    # <a name="retail-73-and-earlier"></a>[Retail 7.3 en eerder](#tab/retail-7-3)

    Verwijder de volgende sectie uit de configuratiebestanden **HardwareStation.Shared.config** en **HardwareStation.Dedicated.config**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-731-and-later"></a>[Retail 7.3.1 en later](#tab/retail-7-3-1)

    Verwijder de volgende sectie van het configuratiebestand **HardwareStation.Extension.config**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample" />
    ```

    # <a name="retail-100-and-later"></a>[Retail 10.0 en later](#tab/retail-10-0)

    Verwijder de volgende sectie van het configuratiebestand **HardwareStation.Extension.config**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.FiscalRegisterSample" />
    ```
    ---

2. Schakel de huidige voorbeeldextensie voor hardwarestations in door de volgende regel toe te voegen aan de sectie **samenstelling** van het configuratiebestand **HardwareStation.Extension.config**.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.CleanCashSample" />
    ```

3. Breng de volgende wijzigingen aan in het configuratiebestand voor pakketaanpassing **Customization.settings** onder de map **BuildTools**:

    - Verwijder de volgende regel om de eerdere extensie voor hardwarestations niet op te nemen in implementeerbare pakketten.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.Extension.FiscalRegisterSample.dll" />
        ```

    - Voeg de volgende regels toe om de huidige voorbeeldextensie voor hardwarestations op te nemen in implementeerbare pakketten.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.CleanCashSample.dll" />
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Interop.CleanCash_1_1.dll" />
        ```

#### <a name="update-modern-pos"></a>Modern POS bijwerken

1. Open de oplossing **cloudPOS.sln** in **RetailSdk\\POS**.
2. Schakel de eerdere POS-extensie uit:

    - Voeg in het bestand **tsconfig.json** de map **FiscalRegisterSample** toe aan de lijst met uitgesloten items.
    - Verwijder de de volgende regels te verwijderen uit het bestand **extensions.json** onder de map **RetailSDK\\POS\\Extensions**.

        ``` json
        {
            "baseUrl": "FiscalRegisterSample"
        }
        ```

3. Schakel de huidige voorbeeldextensie voor POS in door de volgende regels toe te voegen aan het bestand **extensions.json** onder de map **RetailSDK\\POS\\Extensions**.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="update-cloud-pos"></a>Cloud-POS bijwerken

1. Open de oplossing **ModernPOS.sln** onder **RetailSdk\\POS**.
2. Schakel de eerdere POS-extensie uit:

    - Voeg in het bestand **tsconfig.json** de map **FiscalRegisterSample** toe aan de lijst met uitgesloten items.
    - Verwijder de de volgende regels te verwijderen uit het bestand **extensions.json** onder de map **RetailSDK\\POS\\Extensions**.

        ``` json
        {
            "baseUrl": "FiscalRegisterSample"
        }
        ```

3. Schakel de huidige voorbeeldextensie voor POS in door de volgende regels toe te voegen aan het bestand **extensions.json** onder de map **RetailSDK\\POS\\Extensions**.

    ``` json
    {
        "extensionPackages": [
            {
                "baseUrl": "Microsoft/AuditEvent.SE"
            }
        ]
    }
    ```

#### <a name="create-deployable-packages"></a>Implementeerbare pakketten maken

Voer **msbuild** uit voor de hele Retail SDK om implementeerbare pakketten te maken. Pas de pakketten toe via LCS of handmatig. Zie [Verpakking van Retail SDK](../dev-itpro/retail-sdk/retail-sdk-packaging.md) voor meer informatie.
