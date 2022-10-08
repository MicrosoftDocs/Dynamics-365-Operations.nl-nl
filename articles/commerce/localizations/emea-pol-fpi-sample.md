---
title: Voorbeeld van integratie van fiscale printer voor Polen
description: Dit artikel biedt een overzicht van het fiscale integratievoorbeeld voor Polen in Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 10/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-02-01.
ms.openlocfilehash: 2f27e5fdcd2b26a0a1651f21436cb4caad501cf8
ms.sourcegitcommit: 2bc6680dc6b12d20532d383a0edb84d180885b62
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/06/2022
ms.locfileid: "9631366"
---
# <a name="fiscal-printer-integration-sample-for-poland"></a>Voorbeeld van integratie van fiscale printer voor Polen

[!include [banner](../includes/banner.md)]

Dit artikel biedt een overzicht van het fiscale integratievoorbeeld voor Polen in Microsoft Dynamics 365 Commerce.

De Dynamics 365 Commerce-functionaliteit voor Polen omvat een voorbeeldintegratie van het verkooppunt (POS) met een fiscale printer. Het voorbeeld breidt de [functionaliteit voor fiscale integratie](fiscal-integration-for-retail-channel.md) uit en ondersteunt het POSNET ERP 2.02-protocol voor fiscale printers van [Posnet Polska S.A.](https://www.posnet.com.pl) Het voorbeeld maakt communicatie mogelijk met een fiscale printer die met behulp van een native softwarestuurprogramma via een COM-poort is verbonden. Het is geïmplementeerd en getest met een software-emulator die Posnet heeft geleverd voor de Posnet Thermal HD FV EJ fiscale printer. Het voorbeeld wordt geleverd in de vorm van broncode en maakt deel uit van de Commerce Software Development Kit (SDK).

Microsoft brengt geen hardware, software of documentatie van Posnet uit. Neem contact op met [Posnet Polska S.A](https://www.posnet.com.pl) voor informatie over het verkrijgen van de fiscale printer en de werking ervan

## <a name="scenarios"></a>Scenario's

De volgende scenario's worden gedekt door het voorbeeld van de integratie van fiscale printers voor Polen:

- Verkoopscenario's:

    - Een fiscaal ontvangstbewijs afdrukken voor contante verkopen en retouren.
    - Een respons van de fiscale printer vastleggen en opslaan in de kanaaldatabase.
    - Btw:

        - Belastingcodes (afdelingen) toewijzen aan de belastingcodes van de fiscale printer.
        - Toegewezen btw-gegevens overbrengen naar de fiscale printer.

    - Betalingen.

        - Toewijzingen uitvoeren aan de de betalingsmethoden van de fiscale printer.
        - Betalingen afdrukken op een fiscaal ontvangstbewijs.
        - Wijzigingsinformatie afdrukken.

    - Regelkortingen afdrukken.
    - Geschenkbonnen:

        - Een uitgegeven/opnieuw aangerekende geschenkbonregel uitsluiten van een fiscaal ontvangstbewijs voor een verkoop.
        - Een betaling afdrukken waarbij een geschenkbon wordt gebruikt als normale betalingsmethode.

    - Fiscale ontvangstbewijzen afdrukken voor klantorderbewerkingen:

        - Er wordt gen fiscaal ontvangstbewijs afgedrukt voor klantorderstortingen.
        - Een fiscaal ontvangstbewijs afdrukken voor het uitvoeren van regels van een hybride klantorder.
        - Een fiscaal ontvangstbewijs afdrukken voor het ophalen van een klantorder.
        - Een fiscaal ontvangstbewijs afdrukken voor een retourorder.

    - De [klantgegevens](emea-pol-customer-information.md) afdrukken die voor een verkooptransactie op een fiscaal ontvangstbewijs zijn opgegeven. Een voorbeeld van deze informatie is het btw-nummer van de klant.

- Eindedagoverzichten (fiscale X- en fiscale Z-rapporten).
- Foutafhandeling, zoals de volgende opties:

    - Fiscale registraties opnieuw proberen als een poging hiertoe mogelijk is, bijvoorbeeld als de fiscale printer geen verbinding heeft, niet gereed is voor afdrukken of niet reageert, de printer geen papier meer heeft of er een papierstoring is.
    - Stel fiscale registratie uit.
    - Fiscale registratie overslaan of de transactie als geregistreerd markeren en informatiecodes opnemen om de reden voor de storing en extra informatie vast te leggen.
    - Controleer de beschikbaarheid van de fiscale printer voordat een nieuwe verkooptransactie wordt geopend of een verkooptransactie wordt afgerond.

### <a name="gift-cards"></a>Geschenkbonnen

Het integratievoorbeeld voor fiscale printers implementeert de volgende regels die betrekking hebben op geschenkbonnen:

- Verkoopregels die zijn gerelateerd aan de bewerkingen *Geschenkbon uitgeven* en *Toevoegen aan geschenkbon* uitsluiten van het fiscale ontvangstbewijs.
- Druk geen fiscaal ontvangstbewijs af als dit alleen uit geschenkbonregels bestaat.
- Het totale bedrag aan geschenkbonnen dat wordt uitgegeven of dat opnieuw wordt aangerekend in een transactie, aftrekken van betalingsregels van het fiscale ontvangstbewijs.
- Berekende correcties van betalingsregels in de kanaaldatabase opslaan met een verwijzing naar een bijbehorende fiscale transactie.
- Betaling per geschenkbon wordt als een normale betaling beschouwd.

### <a name="customer-deposits-and-customer-order-deposits"></a>Klantstortingen en klantorderstortingen

Met de voorbeeld van de integratie van fiscale printers worden de volgende regels geïmplementeerd die zijn gerelateerd aan klantstortingen en klantorderstortingen:

- Er wordt geen fiscale ontvangstbewijs afgedrukt als een transactie een klantstorting is.
- Er wordt geen fiscaal ontvangstbewijs afgedrukt als een transactie alleen een klantorderstorting bevat of een restitutie voor een klantorderstorting.
- Het bedrag afdrukken van de eerder betaalde storting op een fiscaal ontvangstbewijs voor het ophalen van een klantorder.
- Het storingsbedrag van de klantorder aftrekken van betalingsregels wanneer een hybride klantorder wordt gemaakt.
- Berekende correcties van betalingsregels in de kanaaldatabase opslaan met een verwijzing naar een fiscale transactie voor een hybride klantorder.

### <a name="limitations-of-the-sample"></a>Beperkingen van het voorbeeld

- De fiscale printer ondersteunt alleen scenario's waarin de prijs inclusief btw is. Daarom moet de optie **Prijzen inclusief btw** zijn ingesteld op **Ja** voor zowel winkels als klanten.
- Dagelijkse rapporten (fiscaal X-rapport en fiscaal Z-rapport) worden afgedrukt met de ingesloten indeling *Shift-rapport*.
- Het afdrukken van een streepjescode op fiscale ontvangstbewijzen kan een mogelijke aanpassing zijn, omdat deze functie niet wordt ondersteund in de ingesloten indelingen en alleen kan worden geïmplementeerd met het aanpasbare rapport in **Super-indeling**.
- De fiscale printer ondersteunt geen gemengde transacties. De optie **Het combineren van verkopen en retouren in één ontvangstoptie verbieden** moet zijn ingesteld op **Ja** in POS-functionaliteitsprofielen.

## <a name="set-up-fiscal-integration-for-poland"></a>Fiscale integratie instellen voor Polen

Het voorbeeld van integratie van fiscale printers voor Polen is gebaseerd op de [functionaliteit voor fiscale integratie](fiscal-integration-for-retail-channel.md) en maakt deel uit van de Commerce SDK. Het voorbeeld bevindt zich in de map **src\\FiscalIntegration\\Posnet** van de opslagplaats [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Het [voorbeeld](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) bestaat uit een fiscale documentprovider, hetgeen een extensie van de Commerce runtime (CRT) is, en een fiscale connector, die een uitbreiding is van Commerce Hardware Station. Voor meer informatie over het gebruik van de Commerce SDK, gaat u naar [Commerce SDK-voorbeelden en referentiepakketten van GitHub downloaden en NuGet](../dev-itpro/retail-sdk/sdk-github.md) en [Een build-pipeline instellen voor de onafhankelijke verpakkings-SDK](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Het voorbeeld van de belastingprinterintegratie voor Polen is beschikbaar in de Commerce SDK vanaf Commerce versie 10.0.29. In Commercie versie 10.0.28 of eerder moet u de vorige versie van de Retail SDK gebruiken op een virtuele machine voor developers (VM) in Microsoft Dynamics Lifecycle Services (LCS). Zie [Implementatierichtlijnen voor het voorbeeld van integratie van fiscale printers voor Polen (verouderd)](emea-pol-fpi-sample-sdk.md) voor meer informatie.

Voltooi de instellingsstappen voor de fiscale integratie zoals beschreven in [Fiscale integratie voor Commerce-kanalen instellen](setting-up-fiscal-integration-for-retail-channel.md).

1. [Een fiscaal registratieproces instellen](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Maak ook een notitie van de instellingen voor het fiscale registratieproces die [specifiek zijn voor dit voorbeeld van integratie van fiscale printers](#set-up-the-registration-process).
1. [Instellingen voor het afhandelen van fouten uitvoeren](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Fiscale X/Z-rapporten instellen vanaf het POS](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
1. [Handmatige uitvoering van uitgestelde fiscale registratie inschakelen](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-deferred-fiscal-registration).
1. [Kanaalonderdelen configureren](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Het fiscaal registratieproces instellen

Als u het registratieproces wilt inschakelen, voert u de volgende stappen uit om Commerce Headquarters in te stellen. Zie [De fiscale integratie voor Commerce-kanalen instellen](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process) voor meer informatie.

1. Download configuratiebestanden voor de fiscale documentprovider en de fiscale connector:

    1. Open de opslagplaats met [Dynamics 365 Commerce-oplossingen](https://github.com/microsoft/Dynamics365Commerce.Solutions/).
    1. Selecteer een juiste vertakkingsversie voor vrijgave volgens uw SDK/toepassingsversie.
    1. Open **src \> FiscalIntegration \> Posnet**.
    1. Download het configuratiebestand van de fiscale documentprovider op **CommerceRuntime \> DocumentProvider.PosnetSample \> Configuration \> DocumentProviderPosnetSample.xml**.
    1. Download het configuratiebestand van de fiscale connector op **HardwareStation \> ThermalDeviceSample \> Configuration \> ConnectorPosnetThermalFVEJ.xml**.

    > [!NOTE]
    > In Commercie versie 10.0.28 of eerder moet u de vorige versie van de Retail SDK gebruiken op een virtuele machine voor developers in LCS. De configuratiebestanden voor dit voorbeeld van fiscale integratie bevinden zich in de volgende mappen van de Retail SDK op een ontwikkelaars-VM in LCS:
    >
    > - **Configuratiebestand van fiscale documentprovider:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extension.DocumentProvider.PosnetSample\\Configuration\\DocumentProviderPosnetSample.xml
    > - **Configuratiebestand van fiscale connector:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.Posnet.ThermalDeviceSample\\Configuration\\ConnectorPosnetThermalFVEJ.xml

1. Ga naar **Detailhandel en commerce \> Instelling van hoofdkantoor \> Parameters \> Gedeelde Commerce-parameters**. Stel op het tabblad **Algemeen** de optie **Fiscale integratie inschakelen** in op **Ja**.
1. Ga naar **Retail en commerce \> Kanaalinstellingen \> Fiscale integratie \> Fiscale documentproviders** en laad het configuratiebestand voor de fiscale documentprovider die u eerder hebt gedownload.
1. Ga naar **Retail en commerce \> Kanaalinstellingen \> Fiscale integratie \> Fiscale connectors** en laad het configuratiebestand voor de fiscale connector die u eerder hebt gedownload.
1. Ga naar **Retail en Commerce \> Afzetkanaalinstellingen \> Fiscale integratie \> Functionele connectorprofielen**. Maak een nieuw functioneel connectorprofiel. Selecteer de documentprovider en de connector die u eerder hebt geladen. Werk de [instellingen voor gegevenstoewijzing](#default-data-mapping) bij waar nodig.
1. Ga naar **Retail en Commerce \> Afzetkanaalinstellingen \> Fiscale integratie \> Technische connectorprofielen**. Maak een nieuw technisch connectorprofiel en selecteer de fiscale connector die u eerder hebt geladen. Werk de [connectorinstellingen](#fiscal-connector-settings) bij waar nodig.
6. Ga naar **Retail en Commerce \> Afzetkanaalinstellingen \> Fiscale integratie \> Fiscale connectorgroepen**. Maak een nieuwe fiscale connectorgroep voor het functionele connectorprofiel dat u eerder hebt gemaakt.
7. Ga naar **Retail en Commerce \> Afzetkanaalinstellingen \> Fiscale integratie \> Fiscale registratieprocessen**. Maak een nieuw fiscaal registratieproces en een stap in het fiscale registratieproces en selecteer de fiscale connectorgroep die u eerder hebt gemaakt.
8. Ga naar **Retail en Commerce \> Kanaalinstellingen \> POS-instellingen \> POS-profielen \> Functionaliteitsprofielen**. Selecteer een functionaliteitsprofiel dat is gekoppeld aan de winkel waar het registratieproces moet worden geactiveerd. Selecteer op het sneltabblad **Fiscaal registratieproces** het fiscale registratieproces dat u eerder hebt gemaakt.
9. Ga naar **Retail en Commerce \> Kanaalinstellingen \> POS-instellingen \> POS-profielen \> Hardwareprofielen**. Selecteer een hardwareprofiel dat is gekoppeld aan het hardwarestation waarmee de fiscale printer zal worden verbonden. Selecteer op het sneltabblad **Fiscale randapparatuur** het technische connectorprofiel dat u eerder hebt gemaakt.
10. Open de distributieplanning (**Retail en commerce \> Retail en commerce IT \> Distributieplanning**) en selecteer taken **1070** en **1090** om gegevens ovedr te dragen naar de kanaaldatabase.

#### <a name="default-data-mapping"></a>Standaardgegevenstoewijzing

De volgende standaardgegevenstoewijzing is opgenomen in de configuratie van de fiscale documentprovider die wordt opgegeven als onderdeel van het voorbeeld van fiscale integratie:

- **Btw-percentagetoewijzing**: de toewijzing van btw-percentagewaarden die voor de btw-codes zijn ingesteld aan de specifieke btw-tarieven voor fiscale printers. Hier is de standaardtoewijzing:

    ```
    0 : 23.00 ; 1 : 8.00 ; 2 : 5.00 ; 3 : 0.00
    ```

    Het eerste onderdeel in elk paar staat voor een btw-tariefnummer dat is geconfigureerd in de fiscale printer. Het tweede onderdeel vertegenwoordigt het bijbehorende btw-tarief. Zie de documentatie van het POSNET-stuurprogramma voor meer informatie over de configuratie van het btw-tarief voor de fiscale printer.

- **Betalingsmethodetoewijzing**: de toewijzing van betalingsmethoden die zijn geconfigureerd voor de winkel voor betalingsmethoden die worden ondersteund door de fiscale printer. Hier is de standaardtoewijzing:

    ```
    0 : 0 ; 1 : 0 ; 2 : 2 ; 3 : 2 ; 4 : 0 ; 5 : 0 ; 6 : 0 ; 7 : 2 ; 8 : 0
    ```

    Het eerste onderdeel in elk koppel vertegenwoordigt een betalingsmethode die is ingesteld voor de winkel. Het tweede onderdeel vertegenwoordigt het bijbehorende betalingsformulier dat wordt ondersteund door de fiscale printer. Zie de documentatie van het POSNET-stuurprogramma voor meer informatie over betalingsmethoden die door de fiscale printer worden ondersteund. U moet de voorbeeldtoewijzing wijzigen volgens de betalingsmethoden die in de toepassing zijn geconfigureerd.

#### <a name="fiscal-connector-settings"></a>Instellingen voor fiscale connector

De volgende instellingen zijn opgenomen in de configuratie van de fiscale connector die wordt opgegeven als onderdeel van het voorbeeld van fiscale integratie:

- **Verbindingsreeks**: een tekenreeks die de details van de verbinding met het apparaat beschrijft in een indeling die wordt ondersteund door het stuurprogramma. Zie de documentatie over het POSNET-stuurprogramma voor meer informatie.
- **Datum- en tijdsynchronisatie:** een waarde die aangeeft of de datum en tijd van de printer moeten worden gesynchroniseerd met het verbonden hardwarestation.
- **Time-out apparaat**: de hoeveelheid tijd in milliseconden dat het stuurprogramma wacht op een respons van het apparaat. Zie de documentatie over het POSNET-stuurprogramma voor meer informatie.

### <a name="configure-channel-components"></a>Kanaalonderdelen configureren

> [!NOTE]
> - Het voorbeeld van de belastingprinterintegratie voor Polen is beschikbaar in de Commerce SDK vanaf Commerce versie 10.0.29. In Commercie versie 10.0.28 of eerder moet u de vorige versie van de Retail SDK gebruiken op een virtuele machine voor developers in LCS. Zie [Implementatierichtlijnen voor het voorbeeld van integratie van fiscale printers voor Polen (verouderd)](emea-pol-fpi-sample-sdk.md) voor meer informatie.
> - Voorbeelden voor Commerce die in uw omgeving worden geïmplementeerd, worden niet automatisch bijgewerkt wanneer u service- of kwaliteitsupdates toepast op Commerce-onderdelen. U moet de vereiste voorbeelden handmatig bijwerken.

#### <a name="set-up-the-development-environment"></a>De ontwikkelingsomgeving instellen

Voer de volgende stappen uit om een ontwikkelingsomgeving in te stellen zodat u het voorbeeld kunt testen en uitbreiden.

1. Kloon of download de [Dynamics 365 Commerce-oplossingen](https://github.com/microsoft/Dynamics365Commerce.Solutions). Selecteer een juiste vertakkingsversie voor vrijgave volgens uw SDK/toepassingsversie. Zie [Commerce SDK-voorbeelden en referentiepakketten van GitHub downloaden en NuGet](../dev-itpro/retail-sdk/sdk-github.md) voor meer informatie.
1. Open de oplossing voor integratie van fiscale printers op **Dynamics365Commerce.Solutions\\FiscalIntegration\\Posnet\\Posnet.sln** en bouw deze.
1. Installeer CRT-extensies:

    1. Zoek het installatieprogramma voor CRT-extensies:

        - **Commerce Scale Unit:** zoek in de map **Posnet\\ScaleUnit\\ScaleUnit.Posnet.Installer\\bin\\Debug\\net461** het installatieprogramma **ScaleUnit.Posnet.Installer**.
        - **Lokale CRT op Modern POS**: zoek in de map **Posnet\\ModernPOS\\ModernPOS.Posnet.Installer\\bin\\Debug\\net461** het installatieprogramma **ModernPOS.Posnet.Installer**.

    1. Start het installatieprogramma voor CRT-extensies vanaf de opdrachtregel:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.Posnet.Installer.exe install --verbosity 0
            ```

        - **Lokale CRT op Modern POS:**

            ```Console
            ModernPOS.Posnet.Installer.exe install --verbosity 0
            ```

1. Installeer extensies van Hardware Station:

    1. Zoek in de map **Posnet\\HardwareStation\\HardwareStation.PosnetThermalFVFiscalPrinter.Installer\\bin\\Debug\\net461** het installatieprogramma **HardwareStation.PosnetThermalFVFiscalPrinter.Installer**.
    1. Start het installatieprogramma voor extensies vanaf de opdrachtregel:

        ```Console
        HardwareStation.PosnetThermalFVFiscalPrinter.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Productieomgeving

Volg de stappen in [Een bouwpijplijn instellen voor een voorbeeld van fiscale integratie](fiscal-integration-sample-build-pipeline.md) voor het instellen en vrijgeven van de Cloud Scale Unit en selfservice implementeerbare pakketten voor het voorbeeld van fiscale integratie. Het YAML-sjabloonbestand **Posnet build-pipeline.yml** is te vinden in de map **Pipeline\\YAML_Files** van de opslagplaats [Dynamics 365 Commerce-oplossingen](https://github.com/microsoft/Dynamics365Commerce.Solutions).

## <a name="design-of-extensions"></a>Ontwerp van extensies

Het voorbeeld van integratie van fiscale printers voor Polen is gebaseerd op de [functionaliteit voor fiscale integratie](fiscal-integration-for-retail-channel.md) en maakt deel uit van de Commerce SDK. Het voorbeeld bevindt zich in de map **src\\FiscalIntegration\\Posnet** van de opslagplaats [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Het [voorbeeld](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) bestaat uit een fiscale documentprovider, die een extensie van CRT is, en een fiscale connector, die een extensie is van Commerce Hardware Station. Voor meer informatie over het gebruik van de Commerce SDK, gaat u naar [Commerce SDK-voorbeelden en referentiepakketten van GitHub downloaden en NuGet](../dev-itpro/retail-sdk/sdk-github.md) en [Een build-pipeline instellen voor de onafhankelijke verpakkings-SDK](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Het voorbeeld van de belastingprinterintegratie voor Polen is beschikbaar in de Commerce SDK vanaf Commerce versie 10.0.29. In Commercie versie 10.0.28 of eerder moet u de vorige versie van de Retail SDK gebruiken op een virtuele machine voor developers in LCS. Zie [Implementatierichtlijnen voor het voorbeeld van integratie van fiscale printers voor Polen (verouderd)](emea-pol-fpi-sample-sdk.md) voor meer informatie.

### <a name="commerce-runtime-extension-design"></a>Ontwerp van Commerce runtime-extensie

De extensie die een fiscale documentprovider is, heeft tot doel om printerspecifieke documenten te genereren en responsen van de fiscale printer af te handelen. Met deze extensie genereert u een set printerspecifieke opdrachten in de JSON-indeling (JavaScript Object Notation) die zijn gedefinieerd door POSNET-specificatie 19-3678.

#### <a name="request-handler"></a>Aanvraaghandler

De aanvraaghandler **DocumentProviderPosnetProtocol** is het invoerpunt voor de aanvraag om documenten te genereren vanuit de fiscale printer.

De handler wordt overgenomen van de interface **INamedRequestHandler**. De methode **HandlerName** is verantwoordelijk voor het retourneren van de naam van de handler. De handlernaam moet overeenkomen met de naam van de connector-documentprovider die is opgegeven in Commerce Headquarters.

De connector ondersteunt de volgende aanvragen:

- **GetFiscalDocumentDocumentProviderRequest**: deze aanvraag bevat informatie over welk document moet worden gegenereerd. Het retourneert een printerspecifieke document dat in de fiscale printer moet worden geregistreerd.
- **GetSupportedRegistrableEventsDocumentProviderRequest**: met deze aanvraag retourneert u de lijst met gebeurtenissen waarop u een abonnement wilt nemen. Op dit moment worden de volgende gebeurtenissen ondersteund: verkopen, X-rapport afdrukken en Z-rapport afdrukken.

#### <a name="configuration"></a>Configuratie

Het configuratiebestand voor de fiscale documentprovider bevindt zich in **src\\FiscalIntegration\\Posnet\\CommerceRuntime\\DocumentProvider.PosnetSample\\Configuration\\DocumentProviderPosnetSample.xml** in de opslagplaats [Dynamics 365 Commerce-oplossingen](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Het doel van het bestand is het inschakelen van instellingen van de fiscale documentprovider die moeten worden geconfigureerd vanuit Commerce Headquarters. De bestandsindeling is afgestemd op de vereisten voor de configuratie van fiscale integratie.

### <a name="hardware-station-extension-design"></a>Ontwerp van extensies voor hardwarestation

De extensie die een fiscale connector is, heeft tot doel om te communiceren met de fiscale printer. Met deze extensie worden de functies van het POSNET-stuurprogramma aangeroepen om opdrachten die de CRT-extensie genereert in te dienen bij de fiscale printer. Ook apparaatfouten worden afgehandeld.

#### <a name="request-handler"></a>Aanvraaghandler

De aanvraaghandler **FiscalPrinterHandler** is het invoerpunt voor het verwerken van de aanvraag voor het fiscale randapparaat.

De handler wordt overgenomen van de interface **INamedRequestHandler**. De methode **HandlerName** is verantwoordelijk voor het retourneren van de naam van de handler. De handlernaam moet overeenkomen met de naam van de fiscale connector die is opgegeven in Commerce Headquarters.

De connector ondersteunt de volgende aanvragen:

- **SubmitDocumentFiscalDeviceRequest**: met deze aanvraag worden documenten naar de printers verzonden en wordt de respons van de fiscale printer geretourneerd.
- **IsReadyFiscalDeviceRequest**: deze aanvraag wordt gebruikt voor een statuscontrole van het apparaat.
- **InitializeFiscalDeviceRequest**: deze aanvraag wordt gebruikt voor initialisatie van de printer.

#### <a name="configuration"></a>Configuratie

Het configuratiebestand voor de fiscale connector bevindt zich op **src\\FiscalIntegration\\Posnet\\HardwareStation\\ThermalDeviceSample\\Configuration\\ConnectorPosnetThermalFVEJ.xml** in de opslagplaats [Dynamics 365 Commerce-oplossingen](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Het doel van het bestand is het inschakelen van instellingen van de fiscale connector die moet worden geconfigureerd vanuit Commerce Headquarters. De bestandsindeling is afgestemd op de vereisten voor de configuratie van fiscale integratie.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
