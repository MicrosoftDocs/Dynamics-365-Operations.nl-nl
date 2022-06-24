---
title: Voorbeeld van integratie van fiscale printer voor Italië
description: Dit artikel biedt een overzicht van het fiscale integratievoorbeeld voor Italië in Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2018-11-1
ms.openlocfilehash: 2aa1851fe5fe447ba2dd4640be9881b37e54216e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909385"
---
# <a name="fiscal-printer-integration-sample-for-italy"></a>Voorbeeld van integratie van fiscale printer voor Italië

[!include[banner](../includes/banner.md)]

Dit artikel biedt een overzicht van het fiscale integratievoorbeeld voor Italië in Microsoft Dynamics 365 Commerce.

De Commerce-functionaliteit voor Italië omvat een voorbeeldintegratie van het verkooppunt (POS) met een fiscale printer. De voorbeeldfunctie is een uitbreiding van de [functionaliteit voor fiscale integratie](fiscal-integration-for-retail-channel.md) zodat deze werkt met printers uit de [Epson FP-90III-reeks](https://www.epson.it/products/sd/pos-printer/epson-fp-90iii-series) en maakt communicatie met een fiscale printer in de webservermodus mogelijk via de webservice EpsonFPMate met behulp van Fiscal ePOS-Print API. Het voorbeeld ondersteunt alleen de RT-modus (Registratore Telematico). Het voorbeeld wordt geleverd in de vorm van broncode en maakt deel uit van de Retail Software Development Kit (SDK).

Microsoft brengt geen hardware, software of documentatie van Epson uit. Neem contact op met [Epson Italia S.p.A](https://www.epson.it) voor informatie over het verkrijgen van de fiscale printer en de werking ervan.

## <a name="scenarios"></a>Scenario's

De volgende scenario's worden gedekt door het voorbeeld van de integratie van fiscale printers voor Italië:

- Verkoopscenario's:

    - Een fiscaal ontvangstbewijs afdrukken voor contante verkopen en retouren.
    - Een respons van de fiscale printer vastleggen en opslaan in de kanaaldatabase.
    - Btw:

        - Belastingcodes (afdelingen) toewijzen aan de belastingcodes van de fiscale printer.
        - Toegewezen btw-gegevens overbrengen naar de fiscale printer.
        - Btw afdrukken op een fiscaal ontvangstbewijs.

    - Betalingen:

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

    - Een streepjescode afdrukken voor het ontvangstbewijsnummer op een fiscaal ontvangstbewijs.
    - De [klantgegevens](emea-ita-customer-information.md) afdrukken die voor een verkooptransactie op een fiscaal ontvangstbewijs zijn opgegeven. Een voorbeeld van deze informatie is de loterijcode van de klant. 

- Eindedagoverzichten (fiscale X- en fiscale Z-rapporten).
- Foutafhandeling, zoals de volgende opties:

    - Fiscale registraties opnieuw proberen als een poging hiertoe mogelijk is, bijvoorbeeld als de fiscale printer geen verbinding heeft, niet gereed is voor afdrukken of niet reageert, de printer geen papier meer heeft of er een papierstoring is.
    - Fiscale registratie uitstellen.
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
- Dagelijkse rapporten (fiscaal X-rapport en fiscaal Z-rapport) worden afgedrukt met de indeling die is ingesloten in de firmware van de fiscale printer.
- De fiscale printer ondersteunt geen gemengde transacties. De optie **Het combineren van verkopen en retouren in één ontvangstoptie verbieden** moet zijn ingesteld op **Ja** in POS-functionaliteitsprofielen.
- Het voorbeeld ondersteunt alleen integratie met een fiscale printer die in de RT-modus (Registratore Telematico) werkt.

## <a name="set-up-fiscal-integration-for-italy"></a>Fiscale integratie instellen voor Italië

Het voorbeeld van integratie van fiscale printers voor Italië is gebaseerd op de [functionaliteit voor fiscale integratie](fiscal-integration-for-retail-channel.md) en maakt deel uit van de Retail SDK. Het voorbeeld bevindt zich in de map **src\\FiscalIntegration\\EpsonFP90IIISample** van de opslagplaats voor [Dynamics 365 Commerce-oplossingen](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (bijvoorbeeld het [voorbeeld in versie/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/EpsonFP90IIISample)). Het voorbeeld [bestaat](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) uit een fiscale documentprovider, hetgeen een extensie van de Commerce runtime (CRT) is, en een fiscale connector, die een uitbreiding is van Commerce Hardware Station. Zie de [retail-SDK-architectuur](../dev-itpro/retail-sdk/retail-sdk-overview.md) [Een buildpijplijn instellen voor de onafhankelijke verpakkings-SDK](../dev-itpro/build-pipeline.md) voor meer informatie over het gebruik van de Retail SDK-architectuur en het instellen van een buildpijplijn voor de onafhankelijke verpakkings SDK.

> [!WARNING]
> Vanwege beperkingen van het [nieuwe onafhankelijke verpakkings- en extensiemodel](../dev-itpro/build-pipeline.md) kan het momenteel niet worden gebruikt voor dit voorbeeld van fiscale integratie. U moet de vorige versie van de Retail SDK gebruiken op een virtuele machine voor developers (VM) in Microsoft Dynamics Lifecycle Services (LCS). Zie [Implementatierichtlijnen voor het voorbeeld van integratie van fiscale printers voor Italië (verouderd)](emea-ita-fpi-sample-sdk.md) voor meer informatie.
>
> Ondersteuning van het nieuwe onafhankelijke verpakkings- en extensiemodel voor voorbeelden van fiscale integratie wordt gepland voor latere versies.

Voltooi de instellingsstappen voor de fiscale integratie zoals beschreven in [Fiscale integratie voor Commerce-kanalen instellen](setting-up-fiscal-integration-for-retail-channel.md).

1. [Een fiscaal registratieproces instellen](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Maak ook een notitie van de instellingen voor het fiscale registratieproces die [specifiek zijn voor dit voorbeeld van integratie van fiscale printers](#set-up-the-registration-process).
1. [Fiscale teksten voor kortingen instellen](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-texts-for-discounts).
1. [Instellingen voor het afhandelen van fouten uitvoeren](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Fiscale X/Z-rapporten instellen vanaf het POS](setting-up-fiscal-integration-for-retail-channel.md#set-up-fiscal-xz-reports-from-the-pos).
1. [Handmatige uitvoering van uitgestelde fiscale registratie inschakelen](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [De functionaliteit voor het beheer van klantgegevens in POS instellen](emea-ita-customer-information.md#setup).
1. [Kanaalonderdelen configureren](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Het fiscaal registratieproces instellen

Als u het registratieproces wilt inschakelen, voert u de volgende stappen uit om Commerce Headquarters in te stellen. Zie [De fiscale integratie voor Commerce-kanalen instellen](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process) voor meer informatie.

1. Download configuratiebestanden voor de fiscale documentprovider en de fiscale connector:

    1. Open de opslagplaats met [Dynamics 365 Commerce-oplossingen](https://github.com/microsoft/Dynamics365Commerce.Solutions/).
    1. Selecteer een juiste vertakkingsversie voor vrijgave volgens uw SDK/toepassingsversie (bijvoorbeeld **[versie/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Open **src \> FiscalIntegration \> EpsonFP90IIISample**.
    1. Download het configuratiebestand van de fiscale documentprovider op **CommerceRuntime \> DocumentProvider.EpsonFP90IIISample \> Configuration \> DocumentProviderEpsonFP90IIISample.xml** (bijvoorbeeld [het bestand voor versie/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/EpsonFP90IIISample/CommerceRuntime/DocumentProvider.EpsonFP90IIISample/Configuration/DocumentProviderEpsonFP90IIISample.xml)).
    1. Download het configuratiebestand van de fiscale connector op **HardwareStation \> EpsonFP90IIIFiscalDeviceSample \> Configuration \> ConnectorEpsonFP90IIISample.xml** (bijvoorbeeld [het bestand voor versie/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/EpsonFP90IIISample/HardwareStation/EpsonFP90IIIFiscalDeviceSample/Configuration/ConnectorEpsonFP90IIISample.xml)).

    > [!WARNING]
    > Vanwege beperkingen van het [nieuwe onafhankelijke verpakkings- en extensiemodel](../dev-itpro/build-pipeline.md) kan het momenteel niet worden gebruikt voor dit voorbeeld van fiscale integratie. U moet de vorige versie van de Retail SDK gebruiken op een VM voor developers in LCS. De configuratiebestanden voor dit voorbeeld van fiscale integratie bevinden zich in de volgende mappen van de Retail SDK op een ontwikkelaars-VM in LCS:
    >
    > - **Configuratiebestand van fiscale documentprovider:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extension.DocumentProvider.EpsonFP90IIISample\\Configuration\\DocumentProviderEpsonFP90IIISample.xml
    > - **Configuratiebestand van fiscale connector:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.EpsonFP90IIIFiscalDeviceSample\\Configuration\\ConnectorEpsonFP90IIISample.xml
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

- **Betalingsmethodetoewijzing**: de toewijzing van betalingsmethoden die zijn geconfigureerd voor de winkel voor betalingstypen die worden ondersteund door de fiscale printer. In het volgende voorbeeld wordt de standaardtoewijzing weergegeven.

    ```JSON
    {"PaymentMethods": [
        {"StorePaymentMethod":"1", "PrinterPaymentType":"0", "PrinterPaymentIndex":"00"},
        {"StorePaymentMethod":"3", "PrinterPaymentType":"2", "PrinterPaymentIndex":"00"},
        {"StorePaymentMethod":"4", "PrinterPaymentType":"2", "PrinterPaymentIndex":"01"},
        {"StorePaymentMethod":"6", "PrinterPaymentType":"0", "PrinterPaymentIndex":"01"},
        {"StorePaymentMethod":"8", "PrinterPaymentType":"6", "PrinterPaymentIndex":"01"}
        ],
        "DepositPaymentMethod": {"PrinterPaymentType":"2", "PrinterPaymentIndex":"00"}}
    ```

    Hier volgt een uitleg van de kenmerken in deze toewijzing:

    - **StorePaymentMethod** is een betalingsmethode die is ingesteld voor de winkel bij het instellen van betalingsmethoden voor **Retail en commerce \> Afzetkanaalinstellingen \> Betalingsmethoden \> Betalingsmethoden**.
    - **PrinterPaymentType** en **PrinterPaymentIndex** zijn het corresponderende betalingstype en de index die zijn gedefinieerd in de documentatie van de fiscale printer van Epson.
    - **DepositPaymentMethod** wordt gebruikt om het betalingstype en de index van een printer op te geven voor het gedeelte van het ophaalbedrag van de klantorder dat wordt vereffend met de klantorderstorting.

    In de volgende tabel wordt weergegeven hoe de voorbeeldtoewijzing van betalingsmethoden overeenkomt met de winkelbetalingsmethoden die zijn geconfigureerd in de standaarddemogegevens.

    | Betaalwijze | Naam betalingsmethode |
    |----------------|---------------------|
    | 1              | Contant                |
    | 3              | Kaart                |
    | 4              | Klantrekening    |
    | 6              | Valuta            |
    | 8              | Geschenkbon           |

    U moet de voorbeeldtoewijzing wijzigen volgens de betalingsmethoden die in de toepassing zijn geconfigureerd.

- **Streepjescodetype voor ontvangstbewijsnummer**: het type streepjescode dat wordt gebruikt om een ontvangstbewijsnummer weer te geven op een fiscaal ontvangstbewijs. De standaardtoewijzing is **CODE128**.
- **Fiscale gegevens in de koptekst van het ontvangstbewijs afdrukken**: als deze parameter is ingeschakeld, worden winkelgegevens afgedrukt op het fiscale ontvangstbewijs. Deze informatie omvat de naam, het adres en het btw-identificatienummer van de winkel en de naam van de kassamedewerker.
- **Afdelingstoewijzing fiscale printer**: – de toewijzing van afdelingen van de fiscale printer aan btw-tarieven, btw-vrijstellingsaarden en producttypen. In het volgende voorbeeld wordt de standaardtoewijzing weergegeven.

    ```JSON
    {"Departments": [
        {"VATRate":"2200", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"01"},
        {"VATRate":"2200", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"02"},
        {"VATRate":"1000", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"03"},
        {"VATRate":"1000", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"04"},
        {"VATRate":"0500", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"05"},
        {"VATRate":"0500", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"06"},
        {"VATRate":"0400", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"07"},
        {"VATRate":"0400", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"08"},
        {"VATRate":"0000", "VATExemptNature":"", "ProductType":"0", "DepartmentNumber":"09"},
        {"VATRate":"0000", "VATExemptNature":"", "ProductType":"1", "DepartmentNumber":"10"},
        {"VATRate":"0000", "VATExemptNature":"NS", "ProductType":"0", "DepartmentNumber":"99"}]}
    ```

    Hier volgt een uitleg van de kenmerken in deze toewijzing:

    - **VATRate** is een ondersteund btw-tarief dat is geconfigureerd als een btw-code. De waarde in de toewijzing heeft twee decimalen, maar geen decimaal scheidingsteken. Bijvoorbeeld: **2200** staat voor 22 procent en **1000** voor 10 procent.
    - **VATExemptNature** is alleen van toepassing wanneer het btw-percentage 0 (nul) is, inclusief gevallen waarin er geen btw is. Op dit moment wordt **VATExemptNature** alleen ondersteund voor geschenkbonnen en moet de waarde in de toewijzing overeenkomen met de waarde van de eigenschap **VATExemptNatureForGiftCard** in het XML-configuratiebestand.
    - **ProductType** is het type product. De waarde **0** staat voor goederen en de waarde **1** voor services.
    - **DepartmentNumber** is het nummer van de afdeling die is geconfigureerd in de printer en die overeenkomt met de vorige drie kenmerken.

    U moet de voorbeeldtoewijzing aanpassen aan de hand van de btw-tarieven die zijn geconfigureerd in de toepassing en de overeenkomstige afdelingen die in uw fiscale printer zijn geconfigureerd.

- **Btw-vrijstellingsaard voor geschenkbon**: de btw-vrijstellingsaard die moet worden toegepast wanneer een geschenkbon wordt uitgegeven of aangevuld. De waarde moet overeenkomen met een vermelding in de afdelingstoewijzing van de fiscale printer. De standaardtoewijzing is **NS**.
- **Gratis artikelen inschakelen:** als deze parameter is ingeschakeld, wordt het speciale kortingscorrectietype *omaggio* ingeschakeld voor artikelen met een korting van 100 procent.
- **Informatiecode voor retourontvangst**: de informatiecode die wordt gebruikt om de oorsprong van een retourtransactie vast te leggen als er geen oorspronkelijke verkoopontvangst is opgegeven. Deze parameter wordt samen met de parameters **Informatiecode voor oorspronkelijke verkoopdatum** en **Retour oorsprongtoewijzing** gebruikt om in de fiscale ontvangst een juist bericht te genereren over de oorsprong van een retourtransactie als er geen oorspronkelijke verkooptransactie bestaat. 

    Deze informatiecode moet worden geconfigureerd zodat de gebruiker een van de mogelijke oorsprongen van retouren in uw winkels kan selecteren of invoeren. De code kan bijvoorbeeld worden geconfigureerd als een lijst met subcodes (zoals **Retour van locatie** of **Retour van kiosk**). De parameter **Retour oorsprongtoewijzing** wordt vervolgens gebruikt om de waarde van de informatiecode om te zetten in een opdracht voor de fiscale printer.

    De informatiecode die is geselecteerd voor **Informatiecode voor retourontvangst** moet worden geconfigureerd als verplichte informatiecode die één keer per verkooptransactie moet worden gebruikt. Deze code moet worden toegewezen als de informatiecode **Product retouneren** in het POS-functionaliteitsprofiel, zodat deze kan worden gebruikt wanneer de bewerking **Product retourneren** wordt uitgevoerd.

    Er wordt geen standaardwaarde opgegeven voor deze toewijzing. U moet een informatiecode selecteren die in uw toepassing is geconfigureerd.

- **Informatiecode voor oorspronkelijke verkoopdatum**: de informatiecode die wordt gebruikt om de oorspronkelijke verkoopdatum van een retourtransactie vast te leggen als er geen oorspronkelijke verkoopontvangstbewijs is opgegeven. Deze parameter wordt samen met de parameters **Informatiecode voor retourontvangst** en **Retour oorsprongtoewijzing** gebruikt om in de fiscale ontvangst een juist bericht te genereren over de oorsprong van een retourtransactie als er geen oorspronkelijke verkooptransactie bestaat.

    De informatiecode moet zo worden geconfigureerd dat het veld **Invoertype** is ingesteld op **Datum**. Deze moet worden geconfigureerd als verplichte informatiecode die één keer per verkooptransactie wordt gebruikt. Deze code moet ook worden toegewezen als de **gekoppelde informatiecode** voor de informatiecode die is geselecteerd voor de informatiecode voor de parameter **Informatiecode voor retourontvangst**, zodat de twee informatiecodes na elkaar worden afgegeven.

    Er wordt geen standaardwaarde opgegeven voor deze toewijzing. U moet een informatiecode selecteren die in uw toepassing is geconfigureerd.

- **Retour oorsprongtoewijzing**: de toewijzing van de retouroorsprongen die wordt gebruikt om de oorsprong van een retourtransactie af te drukken als er geen oorspronkelijke verkoopontvangst is opgegeven. Deze parameter wordt samen met de parameters **Informatiecode voor retourontvangst** en **Informatiecode voor oorspronkelijke verkoopdatum** gebruikt om in de fiscale ontvangst een juist bericht te genereren over de oorsprong van een retourtransactie als er geen oorspronkelijke verkooptransactie bestaat. In het volgende voorbeeld wordt de standaardtoewijzing weergegeven.

    ```JSON
    {"ReturnOrigins": [
        {"ReturnOrigin":"1", "PrinterReturnOrigin":"POS"},
        {"ReturnOrigin":"2", "PrinterReturnOrigin":"ND"}
        ],
        "PrinterReturnOriginWithoutFiscalData":"POS"}
    ```

    Hier volgt een uitleg van de kenmerken in deze toewijzing:

    - **ReturnOrigin** is een van de mogelijke oorsprongen van retouren in uw winkels. De waarde moet overeenkomen met de waarde van de parameter **Informatiecode voor retourontvangst**.
    - **PrinterReturnOrigin** is een van de retouren die de fiscale printer accepteert (**POS**, **VR** of **ND**).
    - **PrinterReturnOriginWithoutFiscalData** is de retouroorsprong die door de fiscale printer wordt geaccepteerd en die overeenkomt met een retourtransactie die is gekoppeld aan een oorspronkelijke verkooptransactie zonder gekoppelde fiscale gegevens, omdat deze niet is geregistreerd via een fiscale printer. In dit geval wordt de oorspronkelijke verkoopdatum aangeduid als de datum van de oorspronkelijke verkooptransactie.

De volgende standaardgegevenstoewijzingen zijn verouderd en worden alleen bewaard voor achterwaartse compatibiliteit:

- Toewijzing van btw-codes
- Depositobetalingstype

#### <a name="fiscal-connector-settings"></a>Instellingen voor fiscale connector

De volgende instellingen zijn opgenomen in de configuratie van de fiscale connector die wordt opgegeven als onderdeel van het voorbeeld van fiscale integratie:

- **Eindpuntadres**: de URL van de printer.
- **Datum- en tijdsynchronisatie:** een waarde die aangeeft of de datum en tijd van de printer moeten worden gesynchroniseerd met het verbonden hardwarestation.

### <a name="configure-channel-components"></a>Kanaalonderdelen configureren

> [!WARNING]
> Vanwege beperkingen van het [nieuwe onafhankelijke verpakkings- en extensiemodel](../dev-itpro/build-pipeline.md) kan het momenteel niet worden gebruikt voor dit voorbeeld van fiscale integratie. U moet de vorige versie van de Retail SDK gebruiken op een VM voor developers in LCS. Zie [Implementatierichtlijnen voor het voorbeeld van integratie van fiscale printers voor Italië (verouderd)](emea-ita-fpi-sample-sdk.md) voor meer informatie.
>
> Ondersteuning van het nieuwe onafhankelijke verpakkings- en extensiemodel voor voorbeelden van fiscale integratie wordt gepland voor latere versies.

#### <a name="set-up-the-development-environment"></a>De ontwikkelingsomgeving instellen

Voer de volgende stappen uit om een ontwikkelingsomgeving in te stellen zodat u het voorbeeld kunt testen en uitbreiden.

1. Kloon of download de [Dynamics 365 Commerce-oplossingen](https://github.com/microsoft/Dynamics365Commerce.Solutions). Selecteer een juiste vertakkingsversie voor vrijgave volgens uw SDK/toepassingsversie. Zie [Retail SDK-voorbeelden en referentiepakketten van GitHub downloaden en NuGet](../dev-itpro/retail-sdk/sdk-github.md) voor meer informatie.
1. Open de oplossing voor integratie van fiscale printers op **Dynamics365Commerce.Solutions\\FiscalIntegration\\EpsonFP90IIISample\\EpsonFP90IIISample.sln** en bouw deze.
1. Installeer CRT-extensies:

    1. Zoek het installatieprogramma voor CRT-extensies:

        - **Commerce Scale Unit:** zoek in de map **EpsonFP90IIISample\\ScaleUnit\\ScaleUnit.EpsonFP90III.Installer\\bin\\Debug\\net461** het installatieprogramma **ScaleUnit.EpsonFP90III.Installer**.
        - **Lokale CRT op Modern POS**: zoek in de map **EpsonFP90IIISample\\ModernPOS\\ModernPOS.EpsonFP90III.Installer\\bin\\Debug\\net461** het installatieprogramma **ModernPOS.EpsonFP90III.Installer**.

    1. Start het installatieprogramma voor CRT-extensies vanaf de opdrachtregel:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.EpsonFP90III.Installer.exe install --verbosity 0
            ```

        - **Lokale CRT op Modern POS:**

            ```Console
            ModernPOS.EpsonFP90III.Installer.exe install --verbosity 0
            ```

1. Installeer extensies van Hardware Station:

    1. Zoek in de map **EpsonFP90IIISample\\HardwareStation\\HardwareStation.EpsonFP90III.Installer\\bin\\Debug\\net461** het installatieprogramma **HardwareStation.EpsonFP90III.Installer**.
    1. Start het installatieprogramma voor extensies vanaf de opdrachtregel:

        ```Console
        HardwareStation.EpsonFP90III.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Productieomgeving

Volg de stappen in [Een bouwpijplijn instellen voor een voorbeeld van fiscale integratie](fiscal-integration-sample-build-pipeline.md) voor het instellen en vrijgeven van de Cloud Scale Unit en selfservice implementeerbare pakketten voor het voorbeeld van fiscale integratie. Het YAML-sjabloonbestand **EpsonFP90III build-pipeline.yml** is te vinden in de map **Pipeline\\YAML_Files** van de opslagplaats [Dynamics 365 Commerce-oplossingen](https://github.com/microsoft/Dynamics365Commerce.Solutions).

## <a name="design-of-extensions"></a>Ontwerp van extensies

Het voorbeeld van integratie van fiscale printers voor Italië is gebaseerd op de [functionaliteit voor fiscale integratie](fiscal-integration-for-retail-channel.md) en maakt deel uit van de Retail SDK. Het voorbeeld bevindt zich in de map **src\\FiscalIntegration\\EpsonFP90IIISample** van de opslagplaats voor [Dynamics 365 Commerce-oplossingen](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (bijvoorbeeld het [voorbeeld in versie/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/EpsonFP90IIISample)). Het voorbeeld [bestaat](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) uit een fiscale documentprovider, die een extensie van CRT is, en een fiscale connector, die een extensie is van Commerce Hardware Station. Zie de [retail-SDK-architectuur](../dev-itpro/retail-sdk/retail-sdk-overview.md) [Een buildpijplijn instellen voor de onafhankelijke verpakkings-SDK](../dev-itpro/build-pipeline.md) voor meer informatie over het gebruik van de Retail SDK-architectuur en het instellen van een buildpijplijn voor de onafhankelijke verpakkings SDK.

> [!WARNING]
> Vanwege beperkingen van het [nieuwe onafhankelijke verpakkings- en extensiemodel](../dev-itpro/build-pipeline.md) kan het momenteel niet worden gebruikt voor dit voorbeeld van fiscale integratie. U moet de vorige versie van de Retail SDK gebruiken op een VM voor developers in LCS. Zie [Implementatierichtlijnen voor het voorbeeld van integratie van fiscale printers voor Italië (verouderd)](emea-ita-fpi-sample-sdk.md) voor meer informatie. Ondersteuning van het nieuwe onafhankelijke verpakkings- en extensiemodel voor voorbeelden van fiscale integratie wordt gepland voor latere versies.

### <a name="commerce-runtime-extension-design"></a>Ontwerp van Commerce runtime-extensie

De extensie die een fiscale documentprovider is, heeft tot doel om printerspecifieke documenten te genereren en responsen van de fiscale printer af te handelen.

#### <a name="request-handler"></a>Aanvraaghandler

De aanvraaghandler **DocumentProviderEpsonFP90III** is het invoerpunt voor de aanvraag om documenten te genereren vanuit de fiscale printer.

De handler wordt overgenomen van de interface **INamedRequestHandler**. De methode **HandlerName** is verantwoordelijk voor het retourneren van de naam van de handler. De handlernaam moet overeenkomen met de naam van de connector-documentprovider die is opgegeven in Commerce Headquarters.

De connector ondersteunt de volgende aanvragen:

- **GetFiscalDocumentDocumentProviderRequest**: deze aanvraag bevat informatie over welk document moet worden gegenereerd. Het retourneert een printerspecifieke document dat in de fiscale printer moet worden geregistreerd.
- **GetSupportedRegistrableEventsDocumentProviderRequest**: met deze aanvraag retourneert u de lijst met gebeurtenissen waarop u een abonnement wilt nemen. Op dit moment worden de volgende gebeurtenissen ondersteund: verkopen, X-rapport afdrukken en Z-rapport afdrukken.

#### <a name="configuration"></a>Configuratie

Het configuratiebestand voor de fiscale documentprovider bevindt zich in **src\\FiscalIntegration\\EpsonFP90IIISample\\CommerceRuntime\\DocumentProvider.EpsonFP90IIISample\\Configuration\\DocumentProviderEpsonFP90IIISample.xml** in de opslagplaats [Dynamics 365 Commerce-oplossingen](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Het doel van het bestand is het inschakelen van instellingen die moeten worden geconfigureerd voor de documentprovider vanuit Commerce Headquarters. De bestandsindeling is afgestemd op de vereisten voor de configuratie van fiscale integratie.

### <a name="hardware-station-extension-design"></a>Ontwerp van extensies voor hardwarestation

De extensie die een fiscale connector is, heeft tot doel om te communiceren met de fiscale printer. Deze extensie gebruikt het HTTP-protocol om documenten die de CRT-extensie genereert in te dienen bij de fiscale printer. Het verwerkt ook de responsen die van de fiscale printer worden ontvangen.

#### <a name="request-handler"></a>Aanvraaghandler

De aanvraaghandler **EpsonFP90IIISample** is het invoerpunt voor het verwerken van aanvragen voor het fiscale randapparaat.

De handler wordt overgenomen van de interface **INamedRequestHandler**. De methode **HandlerName** is verantwoordelijk voor het retourneren van de naam van de handler. De handlernaam moet overeenkomen met de naam van de fiscale connector die is opgegeven in Commerce Headquarters.

De connector ondersteunt de volgende aanvragen:

- **SubmitDocumentFiscalDeviceRequest**: met deze aanvraag worden documenten naar de printers verzonden en wordt de respons van de fiscale printer geretourneerd.
- **IsReadyFiscalDeviceRequest**: deze aanvraag wordt gebruikt voor een statuscontrole van het apparaat.
- **InitializeFiscalDeviceRequest**: deze aanvraag wordt gebruikt voor initialisatie van de printer.

#### <a name="configuration"></a>Configuratie

Het configuratiebestand voor de fiscale connector bevindt zich op **src\\FiscalIntegration\\EpsonFP90IIISample\\HardwareStation\\EpsonFP90IIIFiscalDeviceSample\\Configuration\\ConnectorEpsonFP90IIISample.xml** in de opslagplaats voor [Dynamics 365 Commerce-oplossingen](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Het doel van het bestand is het inschakelen van instellingen voor de connector die moet worden geconfigureerd vanuit Commerce Headquarters. De bestandsindeling is afgestemd op de vereisten voor de configuratie van fiscale integratie.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
