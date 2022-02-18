---
title: Voorbeeld van integratie van fiscale registratieservice voor Oostenrijk
description: Dit onderwerp biedt een overzicht van het fiscale integratievoorbeeld voor Oostenrijk in Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 12/20/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: epopov
ms.search.validFrom: 2019-3-1
ms.openlocfilehash: d720bffb98965bdc0276660d2a2e50d2bf155e74
ms.sourcegitcommit: 5cefe7d2a71c6f220190afc3293e33e2b9119685
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/01/2022
ms.locfileid: "8077160"
---
# <a name="fiscal-registration-service-integration-sample-for-austria"></a>Voorbeeld van integratie van fiscale registratieservice voor Oostenrijk

[!include[banner](../includes/banner.md)]

Dit onderwerp biedt een overzicht van het fiscale integratievoorbeeld voor Oostenrijk in Microsoft Dynamics 365 Commerce.

Als u wilt voldoen aan de lokale fiscale vereisten voor kassa's in Oostenrijk, omvat de Dynamics 365 Retail-functionaliteit voor Oostenrijk een voorbeeldintegratie van het POS (point-of-sale) met een externe fiscale registratieservice. In het voorbeeld wordt de [functionaliteit voor fiscale integratie](fiscal-integration-for-retail-channel.md) uitgebreid. Het is gebaseerd op de [EFR-oplossing (Electronic Fiscal Register)](https://www.efsta.eu/at/fiskalloesungen/oesterreich) van [EFSTA](https://www.efsta.eu/at/) en maakt communicatie met de EFR-service via het HTTPS-protocol mogelijk. De EFR-service moet worden gehost op het retailhardwarestation of op een afzonderlijke machine waarmee verbinding kan worden gemaakt vanuit het hardwarestation. Het voorbeeld wordt geleverd in de vorm van broncode en maakt deel uit van de Retail Software Development Kit (SDK).

Microsoft brengt geen hardware, software of documentatie van EFSTA uit. Neem contact op met [EFSTA](https://www.efsta.eu/at/kontakt) voor informatie over het verkrijgen van de EFR-oplossing en de werking ervan.

## <a name="scenarios"></a>Scenario's

De volgende scenario's worden gedekt door het voorbeeld van de integratie van een fiscale registratieservice voor Oostenrijk:

- Registratie van contanttransacties in de fiscale registratieservice:

    - Het verzenden van gedetailleerde transactiegegevens naar de fiscale registratieservice. Deze gegevens bevatten verkoopregelgegevens en informatie over kortingen, betalingen en btw.
    - Het vastleggen van een antwoord van de fiscale registratieservice. Dit antwoord bevat een digitale handtekening en een koppeling naar de geregistreerde transactie.
    - Het registreren van btw en het toewijzen hiervan aan de belastingcodes van de fiscale registratieservice.
    - Het afdrukken van de QR-code voor een geregistreerde transactie op het ontvangstbewijs.

- Registratie van geschenkbonbewerkingen en klantstortingen als niet-contante transacties in de fiscale registratieservice:

    - Het uitgeven of toevoegen van geld aan een geschenkbon.
    - Het registeren van een klantrekeningstorting.
    - Het registeren van een klantorderstorting.

- Registratie van niet-verkooptransacties en -gebeurtenissen als niet-contante transacties in de fiscale registratieservice:

    - Ploeg openen en Ploeg sluiten
    - Beginbedrag, Wisselgeldinvoer en Betalingsmethode verwijderen
    - Prijsaanpassing
    - Belasting overschrijven
    - Kopie van ontvangstbewijs afdrukken
    - Lade openen
    - X-rapport afdrukken
    - Z-rapport afdrukken

- Het afdrukken van eindedagoverzichten (X/Z-rapporten) met velden die specifiek zijn voor Oostenrijk:

    - Het totale aantal producten of services dat aan klanten is geleverd
    - Opsplitsing van verkopen per btw-tarief
    - Opsplitsing van betalingen per kassier/kassamedewerker
    - Prijskortingen en retouren waardoor de dagelijkse verkoop vermindert
    - Nulverkopen (weggevers)

- Foutafhandeling, zoals de volgende opties:

    - Het opnieuw proberen uit te voeren van de fiscale registratie is mogelijk, bijvoorbeeld als de fiscale registratieservice niet beschikbaar of niet gereed is, of als deze niet reageert.
    - Fiscale registratie uitstellen.
    - Fiscale registratie overslaan of de transactie als geregistreerd markeren en informatiecodes opnemen om de reden voor de storing en extra informatie vast te leggen.
    - Controleer de beschikbaarheid van de fiscale registratieservice voordat een nieuwe verkooptransactie wordt geopend of een verkooptransactie wordt afgerond.

### <a name="gift-cards"></a>Geschenkbonnen

Het integratievoorbeeld voor fiscale registratieservice implementeert de volgende regels die betrekking hebben op geschenkbonnen:

- Verkoopregels die zijn gerelateerd aan de bewerkingen *Geschenkbon uitgeven* en *Toevoegen aan geschenkbon* uitsluiten van een contante transactie. In plaats van deze regels als onderdeel van een contante transactie te registreren, registreert u deze als een afzonderlijke niet-contante transactie in de fiscale registratieservice.
- Druk geen opsplitsing van een btw-groep en een QR-code op een ontvangstbewijs af als het ontvangstbewijs alleen uit geschenkbonregels bestaat.
- Druk het totale bedrag aan geschenkbonnen dat wordt uitgegeven of dat opnieuw wordt aangerekend in een transactie apart af van het bedrag van de contante transactie op het ontvangstbewijs.
- Berekende correcties van betalingsregels in de kanaaldatabase opslaan met een verwijzing naar een bijbehorende fiscale transactie.
- Betaling per geschenkbon wordt als een normale betaling beschouwd.

### <a name="customer-deposits-and-customer-order-deposits"></a>Klantstortingen en klantorderstortingen

Met de voorbeeld van de integratie van fiscale registratieservice worden de volgende regels geïmplementeerd die zijn gerelateerd aan klantstortingen en klantorderstortingen:

- Een niet-contante transactie registreren als een transactie een klantstorting is.
- Een niet-contante transactie registreren als een transactie alleen een klantorderstorting bevat of een restitutie voor een klantorderstorting.
- Het storingsbedrag van de klantorder aftrekken van betalingsregels wanneer een hybride klantorder wordt gemaakt.
- Berekende correcties van betalingsregels in de kanaaldatabase opslaan met een verwijzing naar een fiscale transactie voor een hybride klantorder.

### <a name="limitations-of-the-sample"></a>Beperkingen van het voorbeeld

De fiscale registratieservice ondersteunt alleen scenario's waarin de prijs inclusief btw is. Daarom moet de optie **Prijzen inclusief btw** zijn ingesteld op **Ja** voor zowel winkels als klanten.

## <a name="set-up-commerce-for-austria"></a>Commerce instellen voor Oostenrijk

In deze sectie worden de Commerce-instellingen beschreven die specifiek en aanbevolen zijn voor Oostenrijk. Zie [de startpagina van Commerce](../index.md) voor meer informatie over instellingen.

Als u de functionaliteit die specifiek is voor Oostenrijk wilt gebruiken, moet u de volgende instellingen opgeven:

- Stel in het primaire adres van de rechtspersoon het veld **Land/regio** in op **AUT** (Oostenrijk).
- Stel in het POS-functionaliteitsprofiel van elke winkel die zich in Oostenrijk bevindt het veld **ISO-code** in op **AT** (Oostenrijk).

U moet ook de volgende instellingen opgeven voor Oostenrijk. U moet de juiste distributietaken uitvoeren nadat u de instellingen hebt voltooid.

### <a name="set-up-vat-per-austrian-requirements"></a>Btw instellen volgens de Oostenrijkse vereisten

U moet btw-codes, btw-groepen en btw-groepen voor artikelen maken. U moet ook btw-gegevens instellen voor producten en services. Zie [Btw-overzicht](../../finance/general-ledger/indirect-taxes-overview.md) voor meer informatie over het instellen en gebruiken van btw-functies.

Op ontvangstbewijzen bij verkopen kunt u een afgekorte code afdrukken voor een btw-code (bijvoorbeeld "A" of "B"). Stel deze functionaliteit beschikbaar door het veld **Code afdrukken** in te stellen op de pagina **Btw-codes**.

### <a name="set-up-stores"></a>Winkels instellen

Werk op de pagina **Alle winkels** de winkeldetails bij. Stel met name de volgende parameters in:

- Geef in het veld **Btw-groep** de btw-groep op die moet wordenj gebruikt voor verkopen aan de standaardklant.
- Stel de optie **Prijzen zijn inclusief belasting** in op **Ja**.
- Stel het veld **Naam** in op de bedrijfsnaam. Door deze wijziging zorgt u ervoor dat de bedrijfsnaam op een ontvangstbewijs bij verkopen verschijnt. U kunt ook de bedrijfsnaam als vrije tekst aan de indeling voor ontvangstbewijzen voor verkopen toevoegen.
- Stel het veld **Btw-identificatienummer (TIN)** in op het bedrijfsidentificatienummer. Door deze wijziging zorgt u ervoor dat het identificatienummer van het bedrijf op een ontvangstbewijs bij verkopen verschijnt. U kunt ook het identificatienummer van het bedrijf als vrije tekst aan de indeling voor ontvangstbewijzen voor verkopen toevoegen.

### <a name="set-up-functionality-profiles"></a>Functionaliteitsprofielen instellen

POS-functionaliteitsprofielen instellen:

- Stel op het sneltabblad **Ontvangstbewijsnummering** in door records te maken of bij te werken voor de typen ontvangsttransacties **Verkoop**, **Verkooporder** en **Retour**.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Aangepaste velden configureren zodat ze kunnen worden gebruikt in ontvangstbewijsindelingen

U kunt de taaltekst en aangepaste velden configureren die worden gebruikt in de POS-ontvangstindelingen. Het standaardbedrijf van de gebruiker die de ontvangstbewijsinstellingen maakt, moet dezelfde rechtspersoon zijn waar de taaltekstinstelling is gemaakt. Als alternatief moeten dezelfde taalteksten worden gemaakt in het standaardbedrijf van de gebruiker en in de rechtspersoon van de winkel waarvoor de instelling is gemaakt.

Voeg op de pagina **Taaltekst** de volgende records toe voor de labels van de aangepaste velden voor ontvangstbewijsindelingen. De waarden **Taal-id**, **Tekst-ID** en **Tekst** die in de tabel worden weergegeven, zijn slechts voorbeelden. U kunt ze eenvoudig wijzigen zodat ze aan uw behoeften voldoen. De waarden voor **Tekst-id** die u gebruikt, moeten echter uniek zijn en moeten gelijk zijn aan of groter zijn dan 900001.

Voeg de volgende POS-labels toe aan de sectie **POS** van **Taaltekst** uit de tabel:

| Taal-ID | Tekst-id | Tekst                      |
|-------------|---------|---------------------------|
| nl       | 900001  | QR-code                   |
| nl       | 900002  | Doorlopend nummer         |
| nl       | 900003  | Afdrukcode btw-detailhandel     |
| nl       | 900004  | Totaal (verkoop)             |
| nl       | 900005  | Totale btw (verkopen)         |
| nl       | 900006  | Totale inbegrepen btw (verkopen) |
| nl       | 900007  | Btw-bedrag (verkopen)        |
| nl       | 900008  | Btw-basis (verkopen)         |

Voeg op de pagina **Aangepaste velden** de volgende records toe voor de aangepaste velden voor ontvangstbewijsindelingen. Opmerking: waarden voor **Bijschrifttekst-id** moeten overeenkomen met de waarden voor **tekst-id's** die u hebt opgegeven op de pagina **Taaltekst**:

| Name                 | Type    | Tekst-id bijschrift |
|----------------------|---------|-----------------|
| QRCODE               | Ontvangst | 900001          |
| CONTINUOUSNUMBER     | Ontvangst | 900002          |
| RETAILPRINTCODE      | Ontvangst | 900003          |
| SALESTOTAL           | Ontvangst | 900004          |
| SALESTOTALTAX        | Ontvangst | 900005          |
| SALESTOTALINCLUDETAX | Ontvangst | 900006          |
| SALESTAXAMOUNT       | Ontvangst | 900007          |
| SALESTAXBASIS        | Ontvangst | 900008          |

> [!NOTE]
> Het is belangrijk dat u de juiste aangepaste veldnamen opgeeft, zoals aangegeven in de voorgaande tabel. Een onjuiste aangepaste veldnaam veroorzaakt ontbrekende gegevens in ontvangsten.

### <a name="configure-receipt-formats"></a>Indelingen voor ontvangstbewijzen configureren

Wijzig voor elke vereiste indeling voor ontvangstbewijzen de waarde van het veld **Afdrukgedrag** in **Altijd afdrukken**.

Voeg in de ontwerper van de ontvangstbewijsindeling de volgende aangepaste velden toe aan de juiste ontvangstbewijssecties. Opmerking: veldnamen komen overeen met de taalteksten die u in het vorige gedeelte hebt gedefinieerd.

- **Koptekst:** voeg de volgende velden toe:

    - Velden **Winkelnaam** en **Btw-identiteitsnummer** die worden gebruikt om de bedrijfsnaam en het identiteitsnummer af te drukken op ontvangstbewijzen. U kunt ook de bedrijfsnaam en het identiteitsnummer als vrije tekst aan de indeling voor ontvangstbewijzen voor verkopen toevoegen.
    - Velden **Winkeladres**, **Datum**, **Tijd 24 uur**, **Ontvangstbewijsnummer** en **Registernummer**.
    - Velden **Doorlopend nummer**, voor het identificeren van het nummer van de contante transactie in de fiscale registratieservice.

- **Regels:** voeg de volgende velden toe:

    - **Artikelnaam**.
    - **Hoeveelheid**.
    - **Totale prijs met btw**.
    - **Afdrukcode btw-detailhandel**, waarmee de afgekorte code wordt afgedrukt die overeenkomt met de btw-code die geldt voor het artikel.

- **Voettekst:** voeg de volgende velden toe:

    - Betalingsvelden zodat de betalingsbedragen voor elke betalingsmethode worden afgedrukt. Voeg bijvoorbeeld de velden **Naam van betalingsmethode** en **Bedrag van betalingsmethode** toe aan één regel van de indeling.
    - Veldgroep **Verkooptotaal**:

        - Veld **Totaal (verkopen)**, dat wordt gebruikt om het totale contante verkoopbedrag op het ontvangstbewijs af te drukken. Dit bedrag is exclusief btw. Vooruitbetalingen en bewerkingen voor geschenkbonnen zijn uitgesloten.
        - Veld **Totale inbegrepen btw (verkopen)**, dat wordt gebruikt om het totale contante verkoopbedrag op het ontvangstbewijs af te drukken. Bij dit bedrag is btw inbegrepen. Vooruitbetalingen en bewerkingen voor geschenkbonnen zijn uitgesloten.
        - Veld **Totale btw (verkopen)**, dat wordt gebruikt om het totale btw-bedrag voor contante verkopen op het ontvangstbewijs af te drukken. Vooruitbetalingen en bewerkingen voor geschenkbonnen zijn uitgesloten.

    - Veldgroep **Btw-opsplitsing**. Alle velden in deze veldgroep moeten op één afzonderlijke regel worden afgedrukt.

        - Veld **Btw-id**, dat een standaardveld is waarmee voor elke btw-code een btw-overzicht kan worden afgedrukt. Het veld moet worden toegevoegd aan een nieuwe regel.
        - Veld **Btw-percentage**, dat een standaardveld is dat wordt gebruikt om het effectieve btw-percentage voor de btw-code af te drukken.
        - Veld **Btw-basis (verkopen)**, dat wordt gebruikt om het totale bedrag aan contante verkopen voor de btw-code af te drukken. Vooruitbetalingen en bewerkingen voor geschenkbonnen zijn uitgesloten.
        - Veld **Btw-bedrag (verkopen)**, dat wordt gebruikt om het totale bedrag voor contante verkopen voor de btw-code op het ontvangstbewijs af te drukken.
        - Veld **Afdrukcode btw-detailhandel**, waarmee de afgekorte code wordt afgedrukt die overeenkomt met de btw-code.

    - Veld **QR-code**, dat wordt gebruikt om de verwijzing naar de geregistreerde contante transactie af te drukken in de vorm van een QR-code.

        > [!NOTE]
        > De waarde **QR-code** wordt opgehaald uit het antwoord van het fiscale register. EFR retourneert alleen een QR-code als de waarde van het veld **Kenmerken** in de EFR-configuratie is beschreven in de EFSTA-documentatie. De notatie van de QR-code in het veld **Kenmerken** in de EFR-configuratie moet worden ingesteld op **BMP**.

Zie [Ontvangstbewijsindelingen instellen en ontwerpen](../receipt-templates-printing.md) voor meer informatie over het werken met ontvangstbewijsindelingen.

## <a name="set-up-fiscal-integration-for-austria"></a>Fiscale integratie instellen voor Oostenrijk

Het voorbeeld van integratie van fiscale registratieservice voor Oostenrijk is gebaseerd op de [functionaliteit voor fiscale integratie](fiscal-integration-for-retail-channel.md) en maakt deel uit van de Retail SDK. Het voorbeeld bevindt zich in de map **src\\FiscalIntegration\\Efr** van de opslagplaats voor [Dynamics 365 Commerce-oplossingen](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (bijvoorbeeld het [voorbeeld in versie/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Het voorbeeld [bestaat](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) uit een fiscale documentprovider, hetgeen een extensie van de Commerce runtime (CRT) is, en een fiscale connector, die een uitbreiding is van Commerce Hardware Station. Zie de [retail-SDK-architectuur](../dev-itpro/retail-sdk/retail-sdk-overview.md) [Een buildpijplijn instellen voor de onafhankelijke verpakkings-SDK](../dev-itpro/build-pipeline.md) voor meer informatie over het gebruik van de Retail SDK-architectuur en het instellen van een buildpijplijn voor de onafhankelijke verpakkings SDK.

> [!WARNING]
> Vanwege beperkingen van het [nieuwe onafhankelijke verpakkings- en extensiemodel](../dev-itpro/build-pipeline.md) kan het momenteel niet worden gebruikt voor dit voorbeeld van fiscale integratie. U moet de vorige versie van de Retail SDK gebruiken op een virtuele machine voor developers (VM) in Microsoft Dynamics Lifecycle Services (LCS). Zie [Implementatierichtlijnen voor het voorbeeld van fiscale integratie voor Oostenrijk (verouderd)](emea-aut-fi-sample-sdk.md) voor meer informatie. Ondersteuning van het nieuwe onafhankelijke verpakkings- en extensiemodel voor voorbeelden van fiscale integratie wordt gepland voor latere versies.

Voltooi de instellingsstappen voor de fiscale integratie zoals beschreven in [Fiscale integratie voor Commerce-kanalen instellen](setting-up-fiscal-integration-for-retail-channel.md):

1. [Een fiscaal registratieproces instellen](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Maak ook een notitie van de instellingen voor het fiscale registratieproces die [specifiek zijn voor dit voorbeeld van integratie van fiscale registratieservice](#set-up-the-registration-process).
1. [Instellingen voor het afhandelen van fouten uitvoeren](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Handmatige uitvoering van uitgestelde fiscale registratie inschakelen](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-postponed-fiscal-registration).
1. [Kanaalonderdelen configureren](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Het fiscaal registratieproces instellen

Als u het registratieproces wilt inschakelen, voert u de volgende stappen uit om Commerce Headquarters in te stellen. Zie [De fiscale integratie voor Commerce-kanalen instellen](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process) voor meer informatie.

1. Download configuratiebestanden voor de fiscale documentprovider en de fiscale connector:

    1. Open de opslagplaats met [Dynamics 365 Commerce-oplossingen](https://github.com/microsoft/Dynamics365Commerce.Solutions/).
    1. Selecteer een juiste vertakkingsversie voor vrijgave volgens uw SDK/toepassingsversie (bijvoorbeeld **[versie/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33)**).
    1. Open **src \> FiscalIntegration \> Efr**.
    1. Open **Configuraties \> DocumentProviders** en download de configuratiebestanden voor fiscale documentproviders: **DocumentProviderFiscalEFRSampleAustria.xml** en **DocumentProviderNonFiscalEFRSampleAustria.xml** (bijvoorbeeld [de locatie van de bestanden voor versie/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr/Configurations/DocumentProviders)).
    1. Download het configuratiebestand van de fiscale connector op **Configuraties \> Connectors \> ConnectorEFRSample.xml** (bijvoorbeeld [het bestand voor versie/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/blob/release/9.33/src/FiscalIntegration/Efr/Configurations/Connectors/ConnectorEFRSample.xml)).

    > [!WARNING]
    > Vanwege beperkingen van het [nieuwe onafhankelijke verpakkings- en extensiemodel](../dev-itpro/build-pipeline.md) kan het momenteel niet worden gebruikt voor dit voorbeeld van fiscale integratie. U moet de vorige versie van de Retail SDK gebruiken op een VM voor developers in LCS. De configuratiebestanden voor dit voorbeeld van fiscale integratie bevinden zich in de volgende mappen van de Retail SDK op een ontwikkelaars-VM in LCS:
    >
    > - **Configuratiebestand van fiscale documentproviders:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.EFRSample\\Configuration
    > - **Configuratiebestand voor fiscale connector:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.EFRSample\\Configuration
    > 
    > Ondersteuning van het nieuwe onafhankelijke verpakkings- en extensiemodel voor voorbeelden van fiscale integratie wordt gepland voor latere versies.

1. Ga naar **Detailhandel en commerce \> Instelling van hoofdkantoor \> Parameters \> Gedeelde Commerce-parameters**. Stel op het tabblad **Algemeen** de optie **Fiscale integratie inschakelen** in op **Ja**.
1. Ga naar **Retail en commerce \> Kanaalinstellingen \> Fiscale integratie \> Fiscale documentproviders** en laad de configuratiebestanden voor de fiscale documentprovider die u eerder hebt gedownload.
1. Ga naar **Retail en commerce \> Kanaalinstellingen \> Fiscale integratie \> Fiscale connectors** en laad het configuratiebestand voor de fiscale connector die u eerder hebt gedownload.
1. Ga naar **Retail en Commerce \> Afzetkanaalinstellingen \> Fiscale integratie \> Functionele connectorprofielen**. Maak twee nieuwe connectorfunctionaliteitsprofielen, één voor elke belastingdocumentprovider die u eerder hebt geladen, en selecteer de fiscale connector die u eerder hebt geladen. Werk de [instellingen voor gegevenstoewijzing](#default-data-mapping) bij waar nodig.
1. Ga naar **Retail en Commerce \> Afzetkanaalinstellingen \> Fiscale integratie \> Technische connectorprofielen**. Maak een nieuw technisch connectorprofiel en selecteer de fiscale connector die u eerder hebt geladen. Werk de [connectorinstellingen](#fiscal-connector-settings) bij waar nodig.
1. Ga naar **Retail en Commerce \> Afzetkanaalinstellingen \> Fiscale integratie \> Fiscale connectorgroepen**. Maak twee nieuwe fiscale connectorgroepen, één voor elk functioneel connectorprofiel dat u eerder hebt gemaakt.
1. Ga naar **Retail en Commerce \> Afzetkanaalinstellingen \> Fiscale integratie \> Fiscale registratieprocessen**. Maak een nieuw fiscaal registratieproces en twee stappen in het fiscale registratieproces en selecteer de fiscale connectorgroepen die u eerder hebt gemaakt.
1. Ga naar **Retail en Commerce \> Kanaalinstellingen \> POS-instellingen \> POS-profielen \> Functionaliteitsprofielen**. Selecteer een functionaliteitsprofiel dat is gekoppeld aan de winkel waar het registratieproces moet worden geactiveerd. Selecteer op het sneltabblad **Fiscaal registratieproces** het fiscale registratieproces dat u eerder hebt gemaakt. Als u de registratie van niet-fiscale gebeurtenissen op het POS wilt inschakelen, stelt u op het sneltabblad **Functies** onder **POS** de optie **Controle** in op **Ja**.
1. Ga naar **Retail en Commerce \> Kanaalinstellingen \> POS-instellingen \> POS-profielen \> Hardwareprofielen**. Selecteer een hardwareprofiel dat is gekoppeld aan het hardwarestation waarmee de fiscale printer zal worden verbonden. Selecteer op het sneltabblad **Fiscale randapparatuur** het technische connectorprofiel dat u eerder hebt gemaakt.
1. Open de distributieplanning (**Retail en commerce \> Retail en commerce IT \> Distributieplanning**) en selecteer taken **1070** en **1090** om gegevens ovedr te dragen naar de kanaaldatabase.

#### <a name="default-data-mapping"></a>Standaardgegevenstoewijzing

De volgende standaardgegevenstoewijzing is opgenomen in de configuratie van de fiscale documentprovider die wordt opgegeven als onderdeel van het voorbeeld van fiscale integratie:

- **Btw-percentagetoewijzing**: de toewijzing van btw-percentagewaarden die voor de btw-codes worden ingesteld aan waarden van het kenmerk **TaxG** (btw-groep) in aanvragen die naar de fiscale service worden verzonden. Hier is de standaardtoewijzing:

    ```
    A: 20.00; B: 10.00; C: 13.00; D: 0.00; E: 19.00; F: 7.00
    ```

    Het eerste onderdeel in elk koppel vertegenwoordigt een btw-groep die wordt ondersteund door de fiscale EFR-registratieservice. Het tweede onderdeel vertegenwoordigt het bijbehorende btw-tarief. Zie de [EFR-verwijzing](https://public.efsta.net/efr/) voor meer informatie over btw-groepen die EFR ondersteunt voor Oostenrijk.

#### <a name="fiscal-connector-settings"></a>Instellingen voor fiscale connector

De volgende instellingen zijn opgenomen in de configuratie van de fiscale connector die wordt opgegeven als onderdeel van het voorbeeld van fiscale integratie:

- **Eindpuntadres**: de URL van de fiscale registratieservice.
- **Time-out apparaat**: de hoeveelheid tijd in milliseconden dat de fiscale connector wacht op een respons van de fiscale registratieservice.
- **Meldingen fiscale registratie weergeven**: met deze vlag wordt bepaald of meldingen die worden weergegeven aan de operator voor de fiscale registratieservice moeten worden weergegeven.

### <a name="configure-channel-components"></a>Kanaalonderdelen configureren

> [!WARNING]
> Vanwege beperkingen van het [nieuwe onafhankelijke verpakkings- en extensiemodel](../dev-itpro/build-pipeline.md) kan het momenteel niet worden gebruikt voor dit voorbeeld van fiscale integratie. U moet de vorige versie van de Retail SDK gebruiken op een VM voor developers in LCS. Zie [Implementatierichtlijnen voor het voorbeeld van fiscale integratie voor Oostenrijk (verouderd)](emea-aut-fi-sample-sdk.md) voor meer informatie.
>
> Ondersteuning van het nieuwe onafhankelijke verpakkings- en extensiemodel voor voorbeelden van fiscale integratie wordt gepland voor latere versies.

#### <a name="set-up-the-development-environment"></a>De ontwikkelingsomgeving instellen

Voer de volgende stappen uit om een ontwikkelingsomgeving in te stellen zodat u het voorbeeld kunt testen en uitbreiden.

1. Kloon of download de [Dynamics 365 Commerce-oplossingen](https://github.com/microsoft/Dynamics365Commerce.Solutions). Selecteer een juiste vertakkingsversie voor vrijgave volgens uw SDK/toepassingsversie. Zie [Retail SDK-voorbeelden en referentiepakketten van GitHub downloaden en NuGet](../dev-itpro/retail-sdk/sdk-github.md) voor meer informatie.
1. Open de EFR-oplossing op **Dynamics365Commerce.Solutions\\FiscalIntegration\\Efr\\EFR.sln** en bouw deze.
1. Installeer CRT-extensies:

    1. Zoek het installatieprogramma voor CRT-extensies:

        - **Commerce Scale Unit:** zoek in de map **Efr\\ScaleUnit\\ScaleUnit.EFR.Installer\\bin\\Debug\\net461** het installatieprogramma **ScaleUnit.EFR.Installer**.
        - **Lokale CRT op Modern POS**: zoek in de map **Efr\\ModernPOS\\ModernPOS.EFR.Installer\\bin\\Debug\\net461** het installatieprogramma **ModernPOS.EFR.Installer**.

    1. Start het installatieprogramma voor CRT-extensies vanaf de opdrachtregel:

        - **Commerce Scale Unit:**

            ```Console
            ScaleUnit.EFR.Installer.exe install --verbosity 0
            ```

        - **Lokale CRT op Modern POS:**

            ```Console
            ModernPOS.EFR.Installer.exe install --verbosity 0
            ```

1. Installeer extensies van Hardware Station:

    1. Zoek in de map **Efr\\HardwareStation\\HardwareStation.EFR.Installer\\bin\\Debug\\net461** het installatieprogramma **HardwareStation.EFR.Installer**.
    1. Start het installatieprogramma voor extensies vanaf de opdrachtregel.

        ```Console
        HardwareStation.EFR.Installer.exe install --verbosity 0
        ```

#### <a name="production-environment"></a>Productieomgeving

Volg de stappen in [Een bouwpijplijn instellen voor een voorbeeld van fiscale integratie](fiscal-integration-sample-build-pipeline.md) voor het instellen en vrijgeven van de Cloud Scale Unit en selfservice implementeerbare pakketten voor het voorbeeld van fiscale integratie. Het YAML-sjabloonbestand **EFR build-pipeline.yml** is te vinden in de map **Pipeline\\YAML_Files** van de opslagplaats [Dynamics 365 Commerce-oplossingen](https://github.com/microsoft/Dynamics365Commerce.Solutions).

## <a name="design-of-extensions"></a>Ontwerp van extensies

Het voorbeeld van integratie van fiscale registratieservice voor Oostenrijk is gebaseerd op de [functionaliteit voor fiscale integratie](fiscal-integration-for-retail-channel.md) en maakt deel uit van de Retail SDK. Het voorbeeld bevindt zich in de map **src\\FiscalIntegration\\Efr** van de opslagplaats voor [Dynamics 365 Commerce-oplossingen](https://github.com/microsoft/Dynamics365Commerce.Solutions/) (bijvoorbeeld het [voorbeeld in versie/9.33](https://github.com/microsoft/Dynamics365Commerce.Solutions/tree/release/9.33/src/FiscalIntegration/Efr)). Het voorbeeld [bestaat](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) uit een fiscale documentprovider, die een extensie van CRT is, en een fiscale connector, die een extensie is van Commerce Hardware Station. Zie de [retail-SDK-architectuur](../dev-itpro/retail-sdk/retail-sdk-overview.md) [Een buildpijplijn instellen voor de onafhankelijke verpakkings-SDK](../dev-itpro/build-pipeline.md) voor meer informatie over het gebruik van de Retail SDK-architectuur en het instellen van een buildpijplijn voor de onafhankelijke verpakkings SDK.

> [!WARNING]
> Vanwege beperkingen van het [nieuwe onafhankelijke verpakkings- en extensiemodel](../dev-itpro/build-pipeline.md) kan het momenteel niet worden gebruikt voor dit voorbeeld van fiscale integratie. U moet de vorige versie van de Retail SDK gebruiken op een VM voor developers in LCS. Zie [Implementatierichtlijnen voor het voorbeeld van fiscale integratie voor Oostenrijk (verouderd)](emea-aut-fi-sample-sdk.md) voor meer informatie. Ondersteuning van het nieuwe onafhankelijke verpakkings- en extensiemodel voor voorbeelden van fiscale integratie wordt gepland voor latere versies.

### <a name="commerce-runtime-extension-design"></a>Ontwerp van Commerce runtime-extensie

De extensie die een fiscale documentprovider is, heeft tot doel om servicespecifieke documenten te genereren en responsen van de fiscale registratieservice af te handelen.

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

De configuratiebestanden voor de fiscale documentprovider bevinden zich in de map **src\\FiscalIntegration\\Efr\\Configurations\\DocumentProviders** van de opslagplaats voor [Dynamics 365 Commerce-oplossingen](https://github.com/microsoft/Dynamics365Commerce.Solutions/) :

- **DocumentProviderFiscalEFRSampleAustria**: het configuratiebestand voor de fiscale documentprovider voor fiscale documenten.
- **DocumentProviderNonFiscalEFRSampleAustria**: het configuratiebestand voor de fiscale documentprovider voor niet-fiscale documenten.

Het doel van deze bestanden is het inschakelen van instellingen van de fiscale documentprovider die moeten worden geconfigureerd vanuit Commerce Headquarters. De bestandsindeling is afgestemd op de vereisten voor de configuratie van fiscale integratie.

### <a name="hardware-station-extension-design"></a>Ontwerp van extensies voor hardwarestation

De extensie die een fiscale connector is, heeft tot doel om te communiceren met de fiscale registratieservice. De hardwarestationextensie gebruikt het HTTP-protocol om documenten die de CRT-extensie genereert in te dienen bij de fiscale registratieservice. Het verwerkt ook de responsen die van de fiscale registratieservice worden ontvangen.

#### <a name="request-handler"></a>Aanvraaghandler

De aanvraaghandler **EFRHandler** is het invoerpunt voor het afhandelen van aanvragen bij de fiscale registratieservice.

De handler wordt overgenomen van de interface **INamedRequestHandler**. De methode **HandlerName** is verantwoordelijk voor het retourneren van de naam van de handler. De handlernaam moet overeenkomen met de naam van de fiscale connector die is opgegeven in Commerce Headquarters.

De fiscale connector ondersteunt de volgende aanvragen:

- **SubmitDocumentFiscalDeviceRequest**: met deze aanvraag worden documenten naar de fiscale registratieservice verzonden en wordt hierop een respons geretourneerd.
- **IsReadyFiscalDeviceRequest**: deze aanvraag wordt gebruikt voor een statuscontrole van de fiscale registratieservice.
- **InitializeFiscalDeviceRequest**: deze aanvraag wordt gebruikt om de fiscale registratieservice te initialiseren.

#### <a name="configuration"></a>Configuratie

Het configuratiebestand voor de fiscale connector bevindt zich op **src\\FiscalIntegration\\Efr\\Configurations\\Connectors\\ConnectorEFRSample.xml** in de opslagplaats voor [Dynamics 365 Commerce-oplossingen](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Het doel van het bestand is het inschakelen van instellingen van de fiscale connector die moet worden geconfigureerd vanuit Commerce Headquarters. De bestandsindeling is afgestemd op de vereisten voor de configuratie van fiscale integratie.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
