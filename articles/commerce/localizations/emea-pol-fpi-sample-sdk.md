---
title: Implementatierichtlijnen voor het voorbeeld van integratie van fiscale printers voor Polen (verouderd)
description: Dit artikel bevat richtlijnen voor de implementatie van het voorbeeld voor fiscale printerintegratie voor Polen vanuit de Retail SDK (Software Development Kit) voor Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-03-01
ms.openlocfilehash: 883f09f73e3b372d6896b6702e54e2e664cff4d7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286521"
---
# <a name="deployment-guidelines-for-the-fiscal-printer-integration-sample-for-poland-legacy"></a>Implementatierichtlijnen voor het voorbeeld van integratie van fiscale printers voor Polen (verouderd)

[!include[banner](../includes/banner.md)]

Dit artikel bevat richtlijnen voor de implementatie van het voorbeeld voor integratie van fiscale printer voor Polen vanuit de Microsoft Dynamics 365 Commerce Retail Software Development Kit (SDK) op een virtuele machine (VM) voor een developer in Microsoft Dynamics Lifecycle Services (LCS). Zie [Voorbeeld van integratie van fiscale printer voor Polen](emea-pol-fpi-sample.md) voor meer informatie over dit voorbeeld van fiscale integratie. 

Het voorbeeld van fiscale integratie voor Polen maakt deel uit van de Retail SDK. Zie [Architectuur van Retail SDK (Software Development Kit)](../dev-itpro/retail-sdk/retail-sdk-overview.md) voor informatie over het installeren en gebruiken van de SDK. Dit voorbeeld bestaat uit extensies voor Commerce runtime (CRT) en Hardwarestation. Als u dit voorbeeld wilt uitvoeren, moet u de projecten CRT en Hardwarestation wijzigen en bouwen. Het is raadzaam een niet-geverifieerde Retail SDK te gebruiken om de wijzigingen aan te brengen die in dit artikel worden beschreven. Het wordt ook aangeraden een broncontrolesysteem te gebruiken, zoals Azure DevOps wanneer er nog geen bestanden zijn gewijzigd.

## <a name="development-environment"></a>Ontwikkelingsomgeving

Voer de volgende stappen uit om een ontwikkelingsomgeving in te stellen zodat u het voorbeeld kunt testen en uitbreiden.

### <a name="commerce-runtime-extension-components"></a>Onderdelen van Commerce runtime-extensie

De CRT-extensieonderdelen zijn opgenomen in de Retail SDK. Als u de volgende procedures wilt uitvoeren, opent u de oplossing **CommerceRuntimeSamples.sln** onder **RetailSdk\\SampleExtensions\\CommerceRuntime**.

1. Zoek het project **Runtime.Extensions.DocumentProvider.PosnetSample** en bouw het.
2. Zoek in de map **Extensions.DocumentProvider.PosnetSample\\bin\\Debug** het assemblagebestand **Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll**.
3. Kopieer het assemblagebestand naar de map met CRT-extensies:

    - **Schaaleenheid commerce**: kopieer het bestand naar de map **\\bin\\ext** onder de locatie van de commerce scale unit van Internet Information Services (IIS).
    - **Lokale CRT op Modern POS:** kopieer het bestand naar de map **\\ext** onder de locatie van de lokale CRT-clientbroker.

4. Zoek het extensieconfiguratiebestand voor CRT:

    - **Commerce Scale Unit:** het bestand heeft de naam **commerceruntime.ext.config** en bevindt zich in de map **bin\\ext** onder de locatie van de Commerce Scale Unit van Internet Information Services (IIS).
    - **Lokaal CRT op Modern POS:** het bestand heeft de naam **CommerceRuntime.MPOSOffline.Ext.config** en bevindt zich onder de locatie van de lokale CRT-clientbroker.

5. Registreer de CRT-wijziging in het extensieconfiguratiebestand.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
    ```

6. Start de Commerce-service opnieuw:

    - **Commerce Scale Unit:** start de site van de Commerce-service opnieuw vanuit IIS Manager.
    - **Clientbroker:** beëindig het proces **dllhost.exe** in Taakbeheer en start Modern POS vervolgens opnieuw.

### <a name="hardware-station-extension-components"></a>Onderdelen van extensies voor hardwarestation

De onderdelen van de extensie voor het hardwarestation zijn opgenomen in de Retail SDK. Als u de volgende procedures wilt uitvoeren, opent u de oplossing **HardwareStationSamples.sln** onder **RetailSdk\\SampleExtensions\\HardwareStation**.

1. Zoek het project **HardwareStation.Extension.PosnetThermalFVFiscalPrinterSample** en bouw het.
2. Zoek in de map **Extension.Posnet.ThermalFVFiscalPrinterSample\\bin\\Debug** het assemblagebestand **Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample.dll**.
3. Kopieer het assemblagebestand naar een geïmplementeerde hardwarestationmachine:

    - **Extern hardwarestation**: kopieer het bestand naar de map **bin** onder de locatie van de IIS-hardwarestationsite. Kopieer de printerstuurprogrammabibliotheken (**libposcmbth.dll**, **libcmbth\_serial.dll** en **cmbth\_pl.lng**).

4. Zoek het configuratiebestand voor de extensies van het hardwarestation. Het bestand heeft de naam **HardwareStation.Extension.config**:

    - **Extern hardwarestation:** het bestand bevindt zich onder de locatie van de IIS-hardwarestationsite.

5. Voeg de volgende regel toe aan de sectie **samenstelling** van het configuratiebestand.

    ``` xml
    <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
    ```

6. Start de hardwarestationservice opnieuw:

    - **Extern hardwarestation:** start de site van het hardwarestation opnieuw vanuit IIS Manager.

## <a name="production-environment"></a>Productieomgeving

In de vorige procedure hebt u de extensies ingeschakeld die onderdelen zijn van het voorbeeld van integratie van fiscale registratieservice. Daarnaast moet u deze stappen volgen om implementeerbare pakketten te maken die Commerce-onderdelen bevatten, en om deze pakketten toe te passen in een productieomgeving.

1. Breng de volgende wijzigingen aan in de pakketconfiguratiebestanden onder de map **RetailSdk\\Assets**:

    - Voeg in de configuratiebestanden **commerceruntime.ext.config** en **CommerceRuntime.MPOSOffline.Ext.config** de volgende regel toe aan de sectie **Samenstelling**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample" />
        ```

    - Voeg de volgende regel toe aan de sectie **Samenstelling** van het configuratiebestand **HardwareStation.Extension.config**.

        ``` xml
        <add source="assembly" value="Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample" />
        ```

1. Breng de volgende wijzigingen aan in het configuratiebestand voor pakketaanpassing **Customization.settings** onder de map **BuildTools**:

    - Voeg de volgende regel toe om de CRT-extensie op te nemen in de implementeerbare pakketten.

        ``` xml
        <ISV_CommerceRuntime_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.Runtime.Extensions.DocumentProvider.PosnetSample.dll"/>
        ```

    - Voeg de volgende regel toe om de extensie voor hardwarestations op te nemen in de implementeerbare pakketten.

        ``` xml
        <ISV_HardwareStation_CustomizableFile Include="$(SdkReferencesPath)\Contoso.Commerce.HardwareStation.PosnetThermalFVFiscalPrinterSample.dll"/>
        ```

1. Start de MSBuild-opdrachtprompt voor het hulpprogramma Visual Studio en voer **msbuild** uit onder de map Retail SDK om implementeerbare pakketten te maken.
1. Pas de pakketten toe via LCS of handmatig. Zie [Implementeerbare pakketten maken](../dev-itpro/retail-sdk/retail-sdk-packaging.md) voor meer informatie.

## <a name="design-of-extensions"></a>Ontwerp van extensies

Het voorbeeld van integratie van fiscale printer voor Polen is gebaseerd op de [functionaliteit voor fiscale integratie](fiscal-integration-for-retail-channel.md). Zie het [overzicht van het ontwerp van een voorbeeld voor fiscale integratie](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) voor meer informatie over het ontwerp van de oplossing voor fiscale integratie.

### <a name="commerce-runtime-extension-design"></a>Ontwerp van Commerce runtime-extensie

De extensie die een fiscale documentprovider is, heeft tot doel om printerspecifieke documenten te genereren en responsen van de fiscale printer af te handelen.

De CRT-extensie is **Runtime.Extensions.DocumentProvider.PosnetSample**. Met deze extensie genereert u een set printerspecifieke opdrachten in de JSON-indeling (JavaScript Object Notation) die zijn gedefinieerd door POSNET-specificatie 19-3678.

Zie [Fiscaal registratieproces en fiscale integratievoorbeelden voor fiscale apparaten en services](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) voor meer informatie over het ontwerp van de oplossing voor fiscale integratie.

#### <a name="request-handler"></a>Aanvraaghandler

De aanvraaghandler **DocumentProviderPosnetProtocol** is het invoerpunt voor de aanvraag om documenten te genereren vanuit de fiscale printer.

De handler wordt overgenomen van de interface **INamedRequestHandler**. De methode **HandlerName** is verantwoordelijk voor het retourneren van de naam van de handler. De handlernaam moet overeenkomen met de naam van de connector-documentprovider die is opgegeven in Commerce Headquarters.

De connector ondersteunt de volgende aanvragen:

- **GetFiscalDocumentDocumentProviderRequest**: deze aanvraag bevat informatie over welk document moet worden gegenereerd. Het retourneert een printerspecifieke document dat in de fiscale printer moet worden geregistreerd.
- **GetSupportedRegistrableEventsDocumentProviderRequest**: met deze aanvraag retourneert u de lijst met gebeurtenissen waarop u een abonnement wilt nemen. Op dit moment worden de volgende gebeurtenissen ondersteund: verkopen, X-rapport afdrukken en Z-rapport afdrukken.

#### <a name="configuration"></a>Configuratie

Het configuratiebestand bevindt zich in de map **Configuration** van het extensieproject. Het doel van het bestand is het inschakelen van instellingen die moeten worden geconfigureerd voor de documentprovider vanuit Commerce Headquarters. De bestandsindeling is afgestemd op de vereisten voor de configuratie van fiscale integratie. De volgende instellingen worden toegevoegd:

- Toewijzing van btw-tarieven
- Toewijzing van betalingsmethoden
- Depositobetalingstype

### <a name="hardware-station-extension-design"></a>Ontwerp van extensies voor hardwarestation

De extensie die een fiscale connector is, heeft tot doel om te communiceren met de fiscale printer.

De extensie voor hardwarestations is **HardwareStation.Extension.PosnetThermalFVFiscalPrinterSample**. Met deze extensie worden de functies van het POSNET-stuurprogramma aangeroepen om opdrachten die de CRT-extensie genereert in te dienen bij de fiscale printer. Ook apparaatfouten worden afgehandeld.

#### <a name="request-handler"></a>Aanvraaghandler

De aanvraaghandler **FiscalPrinterHandler** is het invoerpunt voor het verwerken van de aanvraag voor het fiscale randapparaat.

De handler wordt overgenomen van de interface **INamedRequestHandler**. De methode **HandlerName** is verantwoordelijk voor het retourneren van de naam van de handler. De handlernaam moet overeenkomen met de naam van de fiscale connector die is opgegeven in Commerce Headquarters.

De connector ondersteunt de volgende aanvragen:

- **SubmitDocumentFiscalDeviceRequest**: met deze aanvraag worden documenten naar de printers verzonden en wordt de respons van de fiscale printer geretourneerd.
- **IsReadyFiscalDeviceRequest**: deze aanvraag wordt gebruikt voor een statuscontrole van het apparaat.
- **InitializeFiscalDeviceRequest**: deze aanvraag wordt gebruikt voor initialisatie van de printer.

#### <a name="configuration"></a>Configuratie

Het configuratiebestand bevindt zich in de map **Configuration** van het extensieproject. Het doel van het bestand is het inschakelen van instellingen voor de connector die moet worden geconfigureerd vanuit Commerce Headquarters. De bestandsindeling is afgestemd op de vereisten voor de configuratie van fiscale integratie. De volgende instellingen worden toegevoegd:

- **Verbindingsreeks**: een tekenreeks die de details van de verbinding met het apparaat beschrijft in een indeling die wordt ondersteund door het stuurprogramma. Zie de documentatie over het POSNET-stuurprogramma voor meer informatie.
- **Datum- en tijdsynchronisatie:** een waarde die aangeeft of de datum en tijd van de printer moeten worden gesynchroniseerd met het verbonden hardwarestation.
- **Time-out apparaat**: de hoeveelheid tijd in milliseconden dat het stuurprogramma wacht op een respons van het apparaat. Zie de documentatie over het POSNET-stuurprogramma voor meer informatie.
