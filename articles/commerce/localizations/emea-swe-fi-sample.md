---
title: Voorbeeld van regeleenheidintegratie voor Zweden
description: Dit artikel biedt een overzicht van het fiscale integratievoorbeeld voor Zweden in Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-10-08
ms.openlocfilehash: 11ce0b146f2e64092b0d03dc7416660d76380cd0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885397"
---
# <a name="control-unit-integration-sample-for-sweden"></a>Voorbeeld van regeleenheidintegratie voor Zweden

[!include [banner](../includes/banner.md)]

Dit artikel biedt een overzicht van het fiscale integratievoorbeeld voor Zweden in Microsoft Dynamics 365 Commerce.

> [!NOTE]
> Deze voorbeeldfunctionaliteit voor fiscale integratie vervangt het eerdere [voorbeeld voor POS-integratie met regeleenheden voor Zweden](retail-sdk-control-unit-sample.md). Het eerdere voorbeeld maakt geen gebruik van het [fiscale integratieraamwerk](./fiscal-integration-for-retail-channel.md) en is verouderd in latere updates. Zie [Migreren vanuit het eerdere voorbeeld](emea-swe-fi-sample-sdk.md#migrating-from-the-earlier-integration-sample) voor meer informatie over migratie vanuit het eerdere voorbeeld naar het voorbeeld dat overeenkomt met Dynamics 365 Commerce versie **10.0.22 en eerder**.

De Commerce-functionaliteit voor Zweden omvat een voorbeeldintegratie van het POS (point-of-sale) met specifieke fiscale apparaten voor Zweden die ook wel *regeleenheden* worden genoemd. In dit voorbeeld wordt de [functionaliteit voor fiscale integratie](fiscal-integration-for-retail-channel.md) uitgebreid. Er wordt aangenomen dat een regeleenheid fysiek is verbonden met een hardwarestation dat aan het POS is gekoppeld. In dit voorbeeld wordt gebruikgemaakt van de API (Application Programming Interface) van de regeleenheid [CleanCash Type A](https://www.retailinnovation.se/produkter) van Retail Innovation HTT AB. Er wordt gebruikgemaakt van versie 1.1.4 van de CleanCash API.

Het voorbeeld wordt geleverd in de vorm van broncode en maakt deel uit van de Retail Software Development Kit (SDK).

Microsoft brengt geen hardware, software of documentatie van Retail Innovation HTT AB uit. Voor informatie over het verkrijgen van de regeleenheid en de werking hiervan, kunt u contact opnemen met [Retail Innovation HTT AB](https://www.retailinnovation.se/).

## <a name="scenarios"></a>Scenario's

Het integratievoorbeeld voor de regeleenheid voor Zweden omvat de volgende capaciteiten:

- Kopieën van verkopen, retouren en ontvangstbewijzen worden automatisch geregistreerd in een regeleenheid die is verbonden met het hardwarestation dat aan het POS is gekoppeld.
- De controlecode en het fabricagenummer van de regeleenheid voor een geregistreerde transactie worden vastgelegd op de regeleenheid en opgeslagen in de transactie. Deze gegevens worden ook wel een *fiscale respons* genoemd. De fiscale respons kan worden weergegeven op de pagina **Winkeltransacties**.
- Aangepaste velden voor de controlecode en het fabricagenummer van de regeleenheid kunnen aan een ontvangstbewijsindeling worden toegevoegd. Op die manier kunt u de fiscale respons voor een transactie op een ontvangstbewijs afdrukken.
- De fiscale respons op een transactie wordt weergegeven in het kanaalrapport **Elektronisch journaal (Zweden)**.
- Er zijn verschillende opties voor het foutafhandeling beschikbaar. Hieronder volgen een aantal voorbeelden:

    - Fiscale registratie opnieuw proberen, als een poging mogelijk is. U kunt fiscale registraties opnieuw proberen, bijvoorbeeld als de rewgeleenheid niet is verbonden, niet gereed is of niet reageert.
    - Fiscale registratie uitstellen.
    - Fiscale registratie overslaan of de transactie als geregistreerd markeren en informatiecodes opnemen om de reden voor de storing en extra informatie vast te leggen.
    - Controleer de beschikbaarheid van de regeleenheid voordat een nieuwe verkooptransactie wordt geopend of een verkooptransactie wordt afgerond.

### <a name="limitations-of-the-sample"></a>Beperkingen van het voorbeeld

Het integratievoorbeeld voor regeleenheden voor Zweden ondersteunt momenteel geen scenario's voor klantorders.

## <a name="setting-up-the-integration-with-control-units"></a>De integratie instellen met regeleenheden

Zie [Commerce instellen voor Zweden](./emea-swe-cash-registers.md#setting-up-commerce-for-sweden) voor meer informatie over de instelling die is vereist voor Zweden.

### <a name="configuring-swedenspecific-receipts"></a>Specifieke ontvangsten configureren voor Zweden

#### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Aangepaste velden configureren zodat ze kunnen worden gebruikt in ontvangstbewijsindelingen

U kunt de taaltekst en aangepaste velden configureren die worden gebruikt in POS-ontvangstindelingen. Het standaardbedrijf van de gebruiker die de ontvangstbewijsinstellingen maakt, moet dezelfde rechtspersoon zijn waar de taaltekstinstelling is gemaakt. Als alternatief moeten dezelfde taalteksten worden gemaakt in het standaardbedrijf van de gebruiker en in de rechtspersoon van de winkel waarvoor de instelling is gemaakt.

Voeg op de pagina **Taaltekst** de volgende records toe voor de labels van de aangepaste velden voor ontvangstbewijsindelingen. De waarden **Taal-id**, **Tekst-ID** en **Tekst** die in de tabel worden weergegeven, zijn slechts voorbeelden. U kunt ze eenvoudig wijzigen zodat ze aan uw behoeften voldoen. De waarden voor **Tekst-id** die u gebruikt, moeten echter uniek zijn en moeten gelijk zijn aan of groter zijn dan 900001.

Voeg de volgende POS-labels toe in de sectie **POS** van de pagina **Taaltekst**.

| Taal-ID | Tekst-id | Tekst                  |
|-------------|---------|-----------------------|
| nl       | 900001  | Controlecode registreren |
| nl       | 900002  | Registratieapparaat       |

Voeg op de pagina **Aangepaste velden** de volgende records toe voor de aangepaste velden voor ontvangstbewijsindelingen. Opmerking: waarden voor **Bijschrifttekst-id** moeten overeenkomen met de waarden voor **tekst-id's** die u hebt opgegeven op de pagina **Taaltekst**.

| Name                         | Type    | Tekst-id bijschrift |
|------------------------------|---------|-----------------|
| SE_FISCALREGISTERCONTROLCODE | Ontvangst | 900001          |
| SE_FISCALREGISTERID          | Ontvangst | 900002          |

> [!NOTE]
> Het is belangrijk dat u de juiste aangepaste veldnamen opgeeft, zoals aangegeven in de bovenstaande tabel. Een onjuiste aangepaste veldnaam veroorzaakt ontbrekende gegevens in ontvangsten.

#### <a name="configure-receipt-formats"></a>Indelingen voor ontvangstbewijzen configureren

Wijzig voor elke indeling die is vereist voor ontvangstbewijzen de waarde van het veld **Afdrukgedrag** in **Altijd afdrukken**.

Voeg in de ontwerper van de ontvangstbewijsindeling de volgende aangepaste velden toe aan de sectie **Voettekst**. Opmerking: veldnamen komen overeen met de taalteksten die u in de vorige sectie van dit artikel hebt gedefinieerd.

- **Controlecode registeren:** dit veld drukt de controlecode af.
- **Registratieapparaat:** dit veld drukt het fabricagenummer van de regeleenheid af.

Zie [Ontvangstsjablonen en afdrukken](../receipt-templates-printing.md) voor meer informatie over het werken met ontvangstbewijsindelingen.

### <a name="set-up-fiscal-integration-for-sweden"></a>Fiscale integratie instellen voor Zweden

Het voorbeeld van integratie van regeleenheden voor Zweden is gebaseerd op de [functionaliteit voor fiscale integratie](fiscal-integration-for-retail-channel.md) en maakt deel uit van de Retail SDK. Het voorbeeld bevindt zich in de map **src\\FiscalIntegration\\CleanCash** van de opslagplaats voor [Dynamics 365 Commerce-oplossingen](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (bijvoorbeeld het [voorbeeld in versie/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/CleanCash)). Het voorbeeld [bestaat](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) uit een fiscale documentprovider, hetgeen een extensie van de Commerce runtime (CRT) is, en een fiscale connector, die een uitbreiding is van Commerce Hardware Station. Zie de [retail-SDK-architectuur](../dev-itpro/retail-sdk/retail-sdk-overview.md) [Een buildpijplijn instellen voor de onafhankelijke verpakkings-SDK](../dev-itpro/build-pipeline.md) voor meer informatie over het gebruik van de Retail SDK-architectuur en het instellen van een buildpijplijn voor de onafhankelijke verpakkings SDK.

> [!WARNING]
> Vanwege beperkingen van het [nieuwe onafhankelijke verpakkings- en extensiemodel](../dev-itpro/build-pipeline.md) kan het momenteel niet worden gebruikt voor dit voorbeeld van fiscale integratie. U moet de vorige versie van de Retail SDK gebruiken op een virtuele machine voor developers (VM) in Microsoft Dynamics Lifecycle Services (LCS). Zie [Implementatierichtlijnen voor het voorbeeld van integratie van regeleenheden voor Zweden (verouderd)](emea-swe-fi-sample-sdk.md) voor meer informatie.
>
> Ondersteuning van het nieuwe onafhankelijke verpakkings- en extensiemodel voor voorbeelden van fiscale integratie wordt gepland voor latere versies.

Voltooi de instellingsstappen voor de fiscale integratie zoals beschreven in [Fiscale integratie voor Commerce-kanalen instellen](setting-up-fiscal-integration-for-retail-channel.md).

1. [Een fiscaal registratieproces instellen](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Maak ook een notitie van de instellingen voor het fiscale registratieproces die [specifiek zijn voor dit voorbeeld van integratie van regeleenheden](#set-up-the-registration-process).
1. [Instellingen voor het afhandelen van fouten uitvoeren](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Handmatige uitvoering van uitgestelde fiscale registratie inschakelen](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Kanaalonderdelen configureren](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Het fiscaal registratieproces instellen

Als u het registratieproces wilt inschakelen, voert u de volgende stappen uit om Commerce Headquarters in te stellen. Zie [De fiscale integratie voor Commerce-kanalen instellen](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process) voor meer informatie.

1. Download configuratiebestanden voor de fiscale documentprovider en de fiscale connector:

    1. Open de opslagplaats met [Dynamics 365 Commerce-oplossingen](https://github.com/microsoft/Dynamics365Commerce.Solutions/).
    1. Selecteer een juiste vertakkingsversie voor vrijgave volgens uw SDK/toepassingsversie (bijvoorbeeld **[versie/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Open **src \> FiscalIntegration \> CleanCash**.
    1. Download het configuratiebestand van de fiscale documentprovider op **CommerceRuntime \> DocumentProvider.CleanCashSample \> Configuration \> DocumentProviderFiscalCleanCashSample.xml** (bijvoorbeeld [het bestand voor versie/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/CleanCash/CommerceRuntime/DocumentProvider.CleanCashSample/Configuration/DocumentProviderFiscalCleanCashSample.xml)).
    1. Download het configuratiebestand van de fiscale connector op **HardwareStation \> Connector.CleanCashSample \> Configuration \> ConnectorCleanCashSample.xml** (bijvoorbeeld [het bestand voor versie/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/CleanCash/HardwareStation/Connector.CleanCashSample/Configuration/ConnectorCleanCashSample.xml)).

    > [!WARNING]
    > Vanwege beperkingen van het [nieuwe onafhankelijke verpakkings- en extensiemodel](../dev-itpro/build-pipeline.md) kan het momenteel niet worden gebruikt voor dit voorbeeld van fiscale integratie. U moet de vorige versie van de Retail SDK gebruiken op een VM voor developers in LCS. De configuratiebestanden voor dit voorbeeld van fiscale integratie bevinden zich in de volgende mappen van de Retail SDK op een ontwikkelaars-VM in LCS:
    >
    > - **Configuratiebestand van fiscale documentprovider:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.CleanCashSample\\Configuration\\DocumentProviderFiscalCleanCashSample.xml
    > - **Configuratiebestand voor fiscale connector:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.CleanCashSample\\Configuration\\ConnectorCleanCashSample.xml
    > 
    > Ondersteuning van het nieuwe onafhankelijke verpakkings- en extensiemodel voor voorbeelden van fiscale integratie wordt gepland voor latere versies.

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

- **Toewijzing van btw-codes**: met deze toewijzing worden apparaatspecifieke btw-codes ingesteld op overeenkomstige btw-codes. De btw-codetoewijzing moet de volgende indeling hebben:

    ```
    1 : code1 ; 2 : code2
    ```

    Hier volgt een uitleg van deze opmaak:

    - *1* en *2* zijn apparaatspecifieke btw-codes.
    - Een puntkomma (;) wordt gebruikt als scheidingsteken.
    - *code1* en *code2* zijn btw-codes die in Commerce Headquarters zijn geconfigureerd. U moet de voorbeeldtoewijzing wijzigen volgens de btw-codes die in de toepassing zijn geconfigureerd.

    Regeleenheden bieden ondersteuning voor maximaal vier verschillende btw-codes. Daarom kan de btw-codetoewijzing als volgt worden ingesteld:

    ```
    1 : code1 ; 2 : code2 ; 3 : code3 ; 4 : code4
    ```

    > [!NOTE]
    > Er kunnen meerdere btw-codes aan dezelfde apparaatspecifieke btw-code worden toegewezen.

#### <a name="fiscal-connector-settings"></a>Instellingen voor fiscale connector

De volgende instellingen zijn opgenomen in de configuratie van de fiscale connector die wordt opgegeven als onderdeel van het voorbeeld van fiscale integratie:

- **Verbindingsreeks**: de instellingen van de regeleenheid.
- **Time-out**: de hoeveelheid tijd in milliseconden dat het stuurprogramma wacht op een respons van de regeleenheid.

### <a name="configure-channel-components"></a>Kanaalonderdelen configureren

> [!WARNING]
> Vanwege beperkingen van het [nieuwe onafhankelijke verpakkings- en extensiemodel](../dev-itpro/build-pipeline.md) kan het momenteel niet worden gebruikt voor dit voorbeeld van fiscale integratie. U moet de vorige versie van de Retail SDK gebruiken op een VM voor developers in LCS. Zie [Implementatierichtlijnen voor het voorbeeld van integratie van regeleenheden voor Zweden (verouderd)](emea-swe-fi-sample-sdk.md) voor meer informatie.
>
> Ondersteuning van het nieuwe onafhankelijke verpakkings- en extensiemodel voor voorbeelden van fiscale integratie wordt gepland voor latere versies.

#### <a name="set-up-the-development-environment"></a>De ontwikkelingsomgeving instellen

Voer de volgende stappen uit om een ontwikkelingsomgeving in te stellen zodat u het voorbeeld kunt testen en uitbreiden.

1. Kloon of download de [Dynamics 365 Commerce-oplossingen](https://github.com/microsoft/Dynamics365Commerce.Solutions). Selecteer een juiste vertakkingsversie voor vrijgave volgens uw SDK/toepassingsversie. Zie [Retail SDK-voorbeelden en referentiepakketten van GitHub downloaden en NuGet](../dev-itpro/retail-sdk/sdk-github.md) voor meer informatie.
1. Open de oplossing voor integratie van regeleenheden op **Dynamics365Commerce.Solutions\\FiscalIntegration\\CleanCash\\CleanCash.sln** en bouw deze.
1. Installeer CRT-extensies:

    1. Zoek het installatieprogramma voor CRT-extensies:

        - **Commerce Scale Unit:** zoek in de map **CleanCash\\ScaleUnit\\ScaleUnit.CleanCash.Installer\\bin\\Debug\\net461** het installatieprogramma **ScaleUnit.CleanCash.Installer**.
        - **Lokale CRT op Modern POS**: zoek in de map **CleanCash\\ModernPOS\\ModernPOS.CleanCash.Installer\\bin\\Debug\\net461** het installatieprogramma **ModernPOS.CleanCash.Installer**.

    2. Start het installatieprogramma voor CRT-extensies vanaf de opdrachtregel:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.CleanCash.Installer.exe install --verbosity 0
            ```

        - **Lokale CRT op Modern POS:**

            ```Console
            ModernPOS.CleanCash.Installer.exe install --verbosity 0
            ```

1. Installeer extensies van Hardware Station:

    1. Zoek in de map **CleanCash\\HardwareStation\\HardwareStation.CleanCash.Installer\\bin\\Debug\\net461** het installatieprogramma **HardwareStation.CleanCash.Installer**.
    1. Start het installatieprogramma voor extensies vanaf de opdrachtregel:

        ```Console
        HardwareStation.CleanCash.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Productieomgeving

Volg de stappen in [Een bouwpijplijn instellen voor een voorbeeld van fiscale integratie](fiscal-integration-sample-build-pipeline.md) voor het instellen en vrijgeven van de Cloud Scale Unit en selfservice implementeerbare pakketten voor het voorbeeld van fiscale integratie. Het YAML-sjabloonbestand **CleanCash build-pipeline.yml** is te vinden in de map **Pipeline\\YAML_Files** van de opslagplaats [Dynamics 365 Commerce-oplossingen](https://github.com/microsoft/Dynamics365Commerce.Solutions).

## <a name="design-of-the-extensions"></a>Ontwerp van de extensies

Het voorbeeld van integratie van regeleenheden voor Zweden is gebaseerd op de [functionaliteit voor fiscale integratie](fiscal-integration-for-retail-channel.md) en maakt deel uit van de Retail SDK. Het voorbeeld bevindt zich in de map **src\\FiscalIntegration\\CleanCash** van de opslagplaats voor [Dynamics 365 Commerce-oplossingen](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (bijvoorbeeld het [voorbeeld in versie/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/CleanCash)). Het voorbeeld [bestaat](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) uit een fiscale documentprovider, die een extensie van CRT is, en een fiscale connector, die een extensie is van Commerce Hardware Station. Zie de [retail-SDK-architectuur](../dev-itpro/retail-sdk/retail-sdk-overview.md) [Een buildpijplijn instellen voor de onafhankelijke verpakkings-SDK](../dev-itpro/build-pipeline.md) voor meer informatie over het gebruik van de Retail SDK-architectuur en het instellen van een buildpijplijn voor de onafhankelijke verpakkings SDK.

> [!WARNING]
> Vanwege beperkingen van het [nieuwe onafhankelijke verpakkings- en extensiemodel](../dev-itpro/build-pipeline.md) kan het momenteel niet worden gebruikt voor dit voorbeeld van fiscale integratie. U moet de vorige versie van de Retail SDK gebruiken op een VM voor developers in LCS. Zie [Implementatierichtlijnen voor het voorbeeld van integratie van regeleenheden voor Zweden (verouderd)](emea-swe-fi-sample-sdk.md) voor meer informatie. Ondersteuning van het nieuwe onafhankelijke verpakkings- en extensiemodel voor voorbeelden van fiscale integratie wordt gepland voor latere versies.

### <a name="crt-extension-design"></a>Ontwerp van CRT-extensies

De extensie die een fiscale documentprovider is, heeft tot doel om servicespecifieke documenten te genereren en responsen van de regeleenheid af te handelen.

#### <a name="request-handler"></a>Aanvraaghandler

Er is een enkele **DocumentProviderCleanCash**-aanvraaghandler voor de documentprovider. Deze handler wordt gebruikt om belastingdocumenten voor de regeleenheid te genereren.

Deze handler wordt overgenomen van de interface **INamedRequestHandler**. De methode **HandlerName** is verantwoordelijk voor het retourneren van de naam van de handler. De handlernaam moet overeenkomen met de naam van de connector-documentprovider die is opgegeven in Commerce Headquarters.

De connector ondersteunt de volgende aanvragen:

- **GetFiscalDocumentDocumentProviderRequest**: deze aanvraag bevat informatie over welk document moet worden gegenereerd. Het retourneert een servicespecifieke document dat in de regeleenheid moet worden geregistreerd.
- **GetSupportedRegistrableEventsDocumentProviderRequest**: met deze aanvraag retourneert u de lijst met gebeurtenissen waarop u een abonnement wilt nemen. Op dit moment worden verkoopgebeurtenissen en auditgebeurtenissen ondersteund.

#### <a name="configuration"></a>Configuratie

Het configuratiebestand voor de fiscale documentprovider bevindt zich in **src\\FiscalIntegration\\CleanCash\\CommerceRuntime\\DocumentProvider.CleanCashSample\\Configuration\\DocumentProviderFiscalCleanCashSample.xml** in de opslagplaats [Dynamics 365 Commerce-oplossingen](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Het doel van dit bestand is het inschakelen van instellingen die moeten worden geconfigureerd voor de documentprovider vanuit Commerce Headquarters. De bestandsindeling is afgestemd op de vereisten voor de configuratie van fiscale integratie.

### <a name="hardware-station-extension-design"></a>Ontwerp van extensies voor hardwarestation

De extensie die een fiscale connector is, heeft tot doel om te communiceren met de regeleenheid. Het gebruikt het HTTP-protocol om documenten die de CRT-extensie genereert in te dienen bij de regeleenheid. Het verwerkt ook de responsen die van de regeleenheid worden ontvangen.

#### <a name="request-handler"></a>Aanvraaghandler

De aanvraaghandler **CleanCashHandler** is het invoerpunt voor het verwerken van aanvragen voor de regeleenheid.

De handler wordt overgenomen van de interface **INamedRequestHandler**. De methode **HandlerName** is verantwoordelijk voor het retourneren van de naam van de handler. De handlernaam moet overeenkomen met de naam van de fiscale connector die is opgegeven in Commerce Headquarters.

De connector ondersteunt de volgende aanvragen:

- **SubmitDocumentFiscalDeviceRequest**: met deze aanvraag worden documenten naar de regeleenheid verzonden en wordt hierop een respons geretourneerd.
- **IsReadyFiscalDeviceRequest**: deze aanvraag wordt gebruikt voor een statuscontrole van de regeleenheid.
- **InitializeFiscalDeviceRequest**: deze aanvraag wordt gebruikt om de regeleenheid te initialiseren.

#### <a name="configuration"></a>Configuratie

Het configuratiebestand voor de fiscale connector bevindt zich op **src\\FiscalIntegration\\CleanCash\\HardwareStation\\Connector.CleanCashSample\\Configuration\\ConnectorCleanCashSample.xml** in de opslagplaats voor [Dynamics 365 Commerce-oplossingen](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Het doel van het bestand is het inschakelen van instellingen voor de fiscale connector die moet worden geconfigureerd vanuit Commerce Headquarters. De bestandsindeling is afgestemd op de vereisten voor de configuratie van fiscale integratie.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
