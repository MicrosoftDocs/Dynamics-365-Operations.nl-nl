---
title: Implementatierichtlijnen voor het voorbeeld van integratie van fiscale printers voor Italië (verouderd)
description: Dit artikel bevat richtlijnen voor de implementatie van het voorbeeld voor fiscale printerintegratie voor Italië vanuit de Retail SDK (Software Development Kit) voor Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 08/18/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: 275759ffec470c6188f734968f4b18b641a49212
ms.sourcegitcommit: b1df4db7facb5e7094138836c41a65c4a158f01d
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/13/2022
ms.locfileid: "9474148"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-italy-legacy"></a>Implementatierichtlijnen voor het voorbeeld van integratie van fiscale printers voor Italië (verouderd)

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> U moet de richtlijnen in dit artikel alleen volgen als u Microsoft Dynamics 365 Commerce versie 10.0.28 of eerder gebruikt. Vanaf Commerce versie 10.0.29 is het voorbeeld van de belastingprinterintegratie voor Italië beschikbaar in de Commerce SDK. Zie [Kanaalonderdelen configureren](./emea-ita-fpi-sample.md#configure-channel-components) voor meer informatie.

Dit artikel bevat richtlijnen voor de implementatie van het voorbeeld voor integratie van fiscale printer voor Italië vanuit de Dynamics 365 Commerce Retail SDK op een virtuele machine (VM) voor een developer in Microsoft Dynamics Lifecycle Services (LCS). Zie [Voorbeeld van integratie van fiscale printer voor Italië](emea-ita-fpi-sample.md) voor meer informatie over dit voorbeeld van fiscale integratie. 

Het voorbeeld van fiscale integratie voor Italië maakt deel uit van de Retail SDK. Zie [Architectuur van Retail SDK (Software Development Kit)](../dev-itpro/retail-sdk/retail-sdk-overview.md) voor informatie over het installeren en gebruiken van de SDK. Dit voorbeeld bestaat uit extensies voor Commerce runtime (CRT) en Hardwarestation. Als u dit voorbeeld wilt uitvoeren, moet u de projecten CRT en Hardwarestation wijzigen en bouwen. Het is raadzaam een niet-geverifieerde Retail SDK te gebruiken om de wijzigingen aan te brengen die in dit artikel worden beschreven. Het wordt ook aangeraden een broncontrolesysteem te gebruiken, zoals Azure DevOps wanneer er nog geen bestanden zijn gewijzigd.

## <a name="development-environment"></a>Ontwikkelingsomgeving

Voer de volgende stappen uit om een ontwikkelingsomgeving in te stellen zodat u het voorbeeld kunt testen en uitbreiden.

### <a name="commerce-runtime-extension-components"></a>Onderdelen van Commerce runtime-extensie

De CRT-extensieonderdelen zijn opgenomen in de Retail SDK. Als u de volgende procedures wilt uitvoeren, opent u de oplossing **CommerceRuntimeSamples.sln** onder **RetailSdk\\SampleExtensions\\CommerceRuntime**.

1. Zoek het project **Runtime.Extensions.DocumentProvider.EpsonFP90IIISample** en bouw het.
2. Zoek in de map **Extensions.DocumentProvider.EpsonFP90IIISample\\bin\\Debug** het assemblagebestand **Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.dll**.
3. Kopieer het assemblagebestand naar de map met CRT-extensies:

    - **Schaaleenheid commerce**: kopieer het bestand naar de map **\\bin\\ext** onder de locatie van de commerce scale unit van Internet Information Services (IIS).
    - **Lokale CRT op Modern POS:** kopieer het bestand naar de map **\\ext** onder de locatie van de lokale CRT-clientbroker.

4. Zoek het extensieconfiguratiebestand voor CRT:

    - **Commerce Scale Unit:** het bestand heeft de naam **commerceruntime.ext.config** en bevindt zich in de map **bin\\ext** onder de locatie van de Commerce Scale Unit van Internet Information Services (IIS).
    - **Lokaal CRT op Modern POS:** het bestand heeft de naam **CommerceRuntime.MPOSOffline.Ext.config** en bevindt zich onder de locatie van de lokale CRT-clientbroker.

5. Registreer de CRT-wijziging in het extensieconfiguratiebestand.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
    ```

6. Start de Commerce Scale Unit opnieuw:

    - **Commerce Scale Unit:** start de site van de Commerce Scale Unit opnieuw vanuit IIS Manager.
    - **Clientbroker:** beëindig het proces **dllhost.exe** in Taakbeheer en start Modern POS vervolgens opnieuw.

### <a name="hardware-station-extension-components"></a>Onderdelen van extensies voor hardwarestation

De onderdelen van de extensie voor het hardwarestation zijn opgenomen in de Retail SDK. Als u de volgende procedures wilt uitvoeren, opent u de oplossing **HardwareStationSamples.sln** onder **RetailSdk\\SampleExtensions\\HardwareStation**.

1. Zoek het project **HardwareStation.Extensions.EpsonFP90IIIFiscalDeviceSample** en bouw het.
2. Zoek in de map **Extensions.EpsonFP90IIIFiscalDeviceSample\\bin\\Debug** het assemblagebestand **Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample.dll**.
3. Kopieer het assemblagebestand naar een geïmplementeerde hardwarestationmachine:

    - **Extern hardwarestation**: kopieer het bestand naar de map **bin** onder de locatie van de IIS-hardwarestationsite.
    - **Lokaal hardwarestation**: kopieer het bestand naar de locatie van de Modern POS-clientbroker.

4. Zoek het configuratiebestand voor de extensies van het hardwarestation. Het bestand heeft de naam **HardwareStation.Extension.config**:

    - **Extern hardwarestation:** het bestand bevindt zich onder de locatie van de IIS-hardwarestationsite.
    - **Lokaal hardwarestation**: het bestand bevindt zich onder de locatie van de Modern POS-clientbroker.

5. Voeg de volgende sectie toe aan de sectie **samenstelling** van het configuratiebestand.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
    ```

6. Start de hardwarestationservice opnieuw:

    - **Extern hardwarestation:** start de site van het hardwarestation opnieuw vanuit IIS Manager.
    - **Lokaal hardwarestation:** beëindig het proces **dllhost.exe** in Taakbeheer en start Modern POS vervolgens opnieuw.

## <a name="production-environment"></a>Productieomgeving

Volg deze stappen om implementeerbare pakketten te maken die Commerce-onderdelen bevatten en om deze pakketten toe te passen in een productieomgeving.

1. Voltooi de stappen die zijn beschreven in de sectie [Ontwikkelomgeving](#development-environment) eerder in dit artikel.
2. Breng de volgende wijzigingen aan in de pakketconfiguratiebestanden onder de map **RetailSdk\\Assets**:

    1. Voeg in de configuratiebestanden **commerceruntime.ext.config** en **CommerceRuntime.MPOSOffline.Ext.config** de volgende regel toe aan de sectie **Samenstelling**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample" />
        ```

    1. Voeg de volgende regel toe aan de sectie **Samenstelling** van het configuratiebestand **HardwareStation.Extension.config**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample" />
        ```

3. Breng de volgende wijzigingen aan in het configuratiebestand voor pakketaanpassing **Customization.settings** onder de map **BuildTools**:

    1. Voeg de volgende regel toe om de CRT-extensie op te nemen in de implementeerbare pakketten.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.dll"/>
        ```

    1. Voeg de volgende regel toe om de extensie voor hardwarestations op te nemen in de implementeerbare pakketten.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.EpsonFP90IIIFiscalDeviceSample.dll"/>
        ```

4. Maak de volgende wijzigingen in het bestand **Sdk.ModernPos.Shared.csproj** onder de map **Packages\_SharedPackagingprojectComponents** om de resourcebestanden voor Italië op te nemen in implementeerbare pakketten:

    1. Voeg een sectie **ItemGroup** toe met knooppunten die naar de resourcebestanden voor de gewenste vertalingen wijzen. Zorg ervoor dat u de juiste naamruimten en voorbeeldnamen opgeeft. In het volgende voorbeeld worden er resourceknooppunten voor de landinstellingen **it** **IT-CH** toegevoegd.

        ```xml
        <ItemGroup>
            <ResourcesIt Include="$(SdkReferencesPath)\it\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
            <ResourcesItCh Include="$(SdkReferencesPath)\it-CH\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
        </ItemGroup>
        ```

    1. In de sectie **Doelnaam="CopyPackageFiles"** voegt u één regel toe voor elke landnaam, zoals in het volgende voorbeeld wordt weergegeven.

        ```xml
        <Copy SourceFiles="@(ResourcesIt)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\it" SkipUnchangedFiles="true" />
        <Copy SourceFiles="@(ResourcesItCh)" DestinationFolder="$(OutputPath)content.folder\CustomizedFiles\ClientBroker\ext\it-CH" SkipUnchangedFiles="true" />
        ```

5. Maak de volgende wijzigingen in het bestand **Sdk.RetailServerSetup.proj** onder de map **Packages\_SharedPackagingprojectComponents** om de resourcebestanden voor Italië op te nemen in implementeerbare pakketten:

    1. Voeg een sectie **ItemGroup** toe met knooppunten die naar de resourcebestanden voor de gewenste vertalingen wijzen. Zorg ervoor dat u de juiste naamruimten en voorbeeldnamen opgeeft. In het volgende voorbeeld worden er resourceknooppunten voor de landinstellingen **it** **IT-CH** toegevoegd.

        ```xml
        <ItemGroup>
            <ResourcesIt Include="$(SdkReferencesPath)\it\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
            <ResourcesItCh Include="$(SdkReferencesPath)\it-CH\Contoso.Commerce.Runtime.DocumentProvider.EpsonFP90IIISample.resources.dll"/>
        </ItemGroup>
        ```

    1. In de sectie **Doelnaam="CopyPackageFiles"** voegt u één regel toe voor elke landnaam, zoals in het volgende voorbeeld wordt weergegeven.

        ``` xml
        <Copy SourceFiles="@(ResourcesIt)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\it" SkipUnchangedFiles="true" />
        <Copy SourceFiles="@(ResourcesItCh)" DestinationFolder="$(OutputPath)content.folder\RetailServer\Code\bin\ext\it-CH" SkipUnchangedFiles="true" />
        ```

6. Start de MSBuild-opdrachtprompt voor het hulpprogramma Visual Studio en voer vervolgens **msbuild** uit onder de map Retail SDK om implementeerbare pakketten te maken.
7. Pas de pakketten toe via LCS of handmatig. Zie [Implementeerbare pakketten maken](../dev-itpro/retail-sdk/retail-sdk-packaging.md) voor meer informatie.

## <a name="design-of-extensions"></a>Ontwerp van extensies

### <a name="commerce-runtime-extension-design"></a>Ontwerp van Commerce runtime-extensie

De extensie die een fiscale documentprovider is, heeft tot doel om printerspecifieke documenten te genereren en responsen van de fiscale printer af te handelen.

De CRT-extensie is **Runtime.Extensions.DocumentProvider.EpsonFP90IIISample**.

Zie [Fiscaal registratieproces en fiscale integratievoorbeelden voor fiscale apparaten en services](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) voor meer informatie over het ontwerp van de oplossing voor fiscale integratie.

#### <a name="request-handler"></a>Aanvraaghandler

De aanvraaghandler **DocumentProviderEpsonFP90III** is het invoerpunt voor de aanvraag om documenten te genereren vanuit de fiscale printer.

De handler wordt overgenomen van de interface **INamedRequestHandler**. De methode **HandlerName** is verantwoordelijk voor het retourneren van de naam van de handler. De handlernaam moet overeenkomen met de naam van de connector-documentprovider die is opgegeven in Commerce Headquarters.

De connector ondersteunt de volgende aanvragen:

- **GetFiscalDocumentDocumentProviderRequest**: deze aanvraag bevat informatie over welk document moet worden gegenereerd. Het retourneert een printerspecifieke document dat in de fiscale printer moet worden geregistreerd.
- **GetSupportedRegistrableEventsDocumentProviderRequest**: met deze aanvraag retourneert u de lijst met gebeurtenissen waarop u een abonnement wilt nemen. Op dit moment worden de volgende gebeurtenissen ondersteund: verkopen, X-rapport afdrukken en Z-rapport afdrukken.

#### <a name="configuration"></a>Configuratie

Het configuratiebestand bevindt zich in de map **Configuration** van het extensieproject. Het doel van het bestand is het inschakelen van instellingen die moeten worden geconfigureerd voor de documentprovider vanuit Commerce Headquarters. De bestandsindeling is afgestemd op de vereisten voor de configuratie van fiscale integratie. De volgende instellingen worden toegevoegd:

- Toewijzing van btw-codes
- Toewijzing van btw-tarieven
- Toewijzing van betalingsmethoden
- Type streepjescode voor ontvangstbewijsnummer
- Depositobetalingstype

### <a name="hardware-station-extension-design"></a>Ontwerp van extensies voor hardwarestation

De extensie die een fiscale connector is, heeft tot doel om te communiceren met de fiscale printer.

De extensie voor hardwarestations is **HardwareStation.Extension.EpsonFP90IIIFiscalDeviceSample**. Deze extensie gebruikt het HTTP-protocol om documenten die de CRT-extensie genereert in te dienen bij de fiscale printer. Het verwerkt ook de responsen die van de fiscale printer worden ontvangen.

#### <a name="request-handler"></a>Aanvraaghandler

De aanvraaghandler **EpsonFP90IIISample** is het invoerpunt voor het verwerken van aanvragen voor het fiscale randapparaat.

De handler wordt overgenomen van de interface **INamedRequestHandler**. De methode **HandlerName** is verantwoordelijk voor het retourneren van de naam van de handler. De handlernaam moet overeenkomen met de naam van de fiscale connector die is opgegeven in Commerce Headquarters.

De connector ondersteunt de volgende aanvragen:

- **SubmitDocumentFiscalDeviceRequest**: met deze aanvraag worden documenten naar de printers verzonden en wordt de respons van de fiscale printer geretourneerd.
- **IsReadyFiscalDeviceRequest**: deze aanvraag wordt gebruikt voor een statuscontrole van het apparaat.
- **InitializeFiscalDeviceRequest**: deze aanvraag wordt gebruikt voor initialisatie van de printer.

#### <a name="configuration"></a>Configuratie

Het configuratiebestand bevindt zich in de map **Configuration** van het extensieproject. Het doel van het bestand is het inschakelen van instellingen voor de connector die moet worden geconfigureerd vanuit Commerce Headquarters. De bestandsindeling is afgestemd op de vereisten voor de configuratie van fiscale integratie. De volgende instellingen worden toegevoegd:

- **Eindpuntadres**: de URL van de printer.
- **Datum- en tijdsynchronisatie:** een waarde die aangeeft of de datum en tijd van de printer moeten worden gesynchroniseerd met het verbonden hardwarestation.
