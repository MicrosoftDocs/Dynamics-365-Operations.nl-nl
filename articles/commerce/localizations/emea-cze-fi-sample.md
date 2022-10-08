---
title: Voorbeeld van integratie van fiscale registratieservice voor Tsjechië
description: Dit artikel biedt een overzicht van het fiscale integratievoorbeeld voor Tsjechië in Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 10/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-04-01
ms.openlocfilehash: de26b038009d8bf3518c67389c96aade19a0b65b
ms.sourcegitcommit: 2bc6680dc6b12d20532d383a0edb84d180885b62
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/06/2022
ms.locfileid: "9631280"
---
# <a name="fiscal-registration-service-integration-sample-for-the-czech-republic"></a>Voorbeeld van integratie van fiscale registratieservice voor Tsjechië

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Dit artikel biedt een overzicht van het fiscale integratievoorbeeld voor Tsjechië in Microsoft Dynamics 365 Commerce.

Als u wilt voldoen aan de lokale fiscale vereisten voor kassa's in Tsjechië, omvat de Dynamics 365 Commerce-functionaliteit voor Tsjechië een voorbeeldintegratie van het POS (point-of-sale) met een externe fiscale registratieservice. In het voorbeeld wordt de [functionaliteit voor fiscale integratie](fiscal-integration-for-retail-channel.md) uitgebreid. Het is gebaseerd op de [EFR-oplossing (Electronic Fiscal Register)](https://efsta.org/sicherheitsloesungen/) van [EFSTA](https://efsta.org/) en maakt communicatie met de EFR-service via het HTTPS-protocol mogelijk. De EFR-service zorgt voor elektronische registratie van verkoop (Elektronická evidence tržeb \[EET\]). Met andere woorden, het zorgt voor online verzending van de verkoopgegevens naar een fiscale webservice van de belastingdienst. De EFR-service moet worden gehost op het Commerce-hardwarestation of op een afzonderlijke machine waarmee verbinding kan worden gemaakt vanuit het hardwarestation. Het voorbeeld wordt geleverd in de vorm van broncode en maakt deel uit van de Commerce Software Development Kit (SDK).

Microsoft brengt geen hardware, software of documentatie van EFSTA uit. Neem contact op met [EFSTA](https://efsta.org/kontakt/) voor informatie over het verkrijgen van de EFR-oplossing en de werking ervan.

## <a name="scenarios"></a>Scenario's

De volgende scenario's worden gedekt door het voorbeeld van de integratie van een fiscale registratieservice voor Tsjechië.

- Registratie van contanttransacties in de fiscale registratieservice.

    - Het verzenden van gedetailleerde transactiegegevens naar de fiscale registratieservice. Deze gegevens bevatten verkoopregelgegevens en informatie over kortingen, betalingen en btw. De fiscale registratieservice stuurt de gegevens verder naar de webservice van de belastingdienst en ontvangt daarvan een bevestiging die de fiscale identificatiecode van de transactie bevat.
    - Het vastleggen van een antwoord van de fiscale registratieservice. Deze respons omvat fiscale gegevens zoals de fiscale identificatiecode en de beveiligingscode van de transactie enzovoort.
    - De fiscale gegevens voor een geregistreerde transactie afdrukken op het ontvangstbewijs.

- Registratie van geschenkbonbewerkingen en in de fiscale registratieservice.

    - Het uitgeven of toevoegen van geld aan een geschenkbon.
    - Het registeren van een klantrekeningstorting.
    - Een klantorder maken en een storting voor de order registreren.
    - Een klantorder bewerken en de storting voor de order overschrijven.
    - Een klantorder annuleren en de storting voor de order restitueren.

- Foutafhandeling, zoals de volgende opties.

    - Het opnieuw proberen uit te voeren van de fiscale registratie is mogelijk, bijvoorbeeld als de fiscale registratieservice niet beschikbaar of niet gereed is, of als deze niet reageert.
    - Stel fiscale registratie uit.
    - Fiscale registratie overslaan of de transactie als geregistreerd markeren en informatiecodes opnemen om de reden voor de storing en extra informatie vast te leggen.
    - Controleer de beschikbaarheid van de fiscale registratieservice voordat een nieuwe verkooptransactie wordt geopend of een verkooptransactie wordt afgerond.

### <a name="gift-cards"></a>Geschenkbonnen

Het integratievoorbeeld voor fiscale registratieservice implementeert de volgende regels die betrekking hebben op geschenkbonnen.

- Verkoopregels die zijn gerelateerd aan de bewerkingen *Geschenkbon uitgeven* of *Toevoegen aan geschenkbon* in een verkooptransactie, worden met een speciaal kenmerk gemarkeerd wanneer de transactie wordt geregistreerd in de fiscale registratieservice.
- Een betaling met een geschenkbon wordt als een normale betaling beschouwd en is gemarkeerd met een speciaal kenmerk wanneer de transactie wordt geregistreerd in de fiscale registratieservice.

### <a name="customer-account-deposits-and-customer-order-deposits"></a>Klantaccountstortingen en klantorderstortingen

Met de voorbeeld van de integratie van fiscale registratieservice worden de volgende regels geïmplementeerd die zijn gerelateerd aan klantaccountstortingen en klantorderstortingen.

- Een transactie die is gerelateerd aan een klantaccountstorting of een klantorderstorting, wordt in de fiscale registratieservice geregistreerd als één regeltransactie en is gemarkeerd met een speciaal kenmerk. De btw-groep voor storting wordt opgegeven op deze regel.
- Wanneer een hybride klantorder wordt gemaakt, dat wil zeggen een klantorder die producten bevat die door de klant uit de winkel kunnen worden uitgevoerd, naast producten die later worden opgehaald of verzonden, bevat de transactie die is geregistreerd in de fiscale registratieservice regels voor de producten die worden uitgevoerd, plus een regel voor de orderstorting.
- Een betaling van een klantaccount wordt als een normale betaling beschouwd en is gemarkeerd met een speciaal kenmerk wanneer de transactie wordt geregistreerd in de fiscale registratieservice.
- Het stortingsbedrag van de klantorder dat wordt toegepast op een bewerking Ophalen voor een klantorder, wordt als een normale betaling beschouwd en is gemarkeerd met een speciaal kenmerk wanneer de transactie wordt geregistreerd in de fiscale registratieservice.

### <a name="offline-registration"></a>Offlineregistratie

Als het verzenden van transactiegegevens door de fiscale registratieservice niet mogelijk is naar de fiscale webservice van de belastingdienst (bijvoorbeeld vanwege een time-out van de respons) en er een bevestiging wordt ontvangen van de webservice (de fiscale identificatiecode van de transactie), wordt een lokale handtekening voor de transactie gegenereerd en wordt deze en een speciale foutcode in de respons weergegeven. Via de fiscale registratieservice worden transacties in de originele volgorde op de achtergrond teruggezet zodra de netwerkverbinding is hersteld.

### <a name="limitations-of-the-sample"></a>Beperkingen van het voorbeeld

De fiscale registratieservice ondersteunt alleen scenario's waarin de prijs inclusief btw is. Daarom moet de optie **Prijzen inclusief btw** zijn ingesteld op **Ja** voor zowel winkels als klanten.

## <a name="set-up-commerce-for-the-czech-republic"></a>Commerce instellen voor Tsjechië

In deze sectie worden de Commerce-instellingen beschreven die specifiek en aanbevolen zijn voor Tsjechië. Zie [Startpagina voor Commerce](../index.md) voor meer informatie.

Als u de functionaliteit die specifiek is voor Tsjechië wilt gebruiken, moet u de volgende instellingen opgeven.

- Stel in het primaire adres van de rechtspersoon het veld **Land/regio** in op **CZE** (Tsjechië).
- Stel in het POS-functionaliteitsprofiel van elke winkel die zich in Tsjechië bevindt het veld **ISO-code** in op **CZ** (Tsjechië).

U moet ook de volgende instellingen opgeven voor Tsjechië. U moet de juiste distributietaken uitvoeren nadat u de instellingen hebt voltooid.

### <a name="set-up-vat-per-czech-republic-requirements"></a>Btw instellen volgens de vereisten voor Tsjechië


U moet btw-codes, btw-groepen en btw-groepen voor artikelen maken. U moet ook btw-gegevens instellen voor producten en services. Zie [Btw-overzicht](../../finance/general-ledger/indirect-taxes-overview.md) voor meer informatie over het instellen en gebruiken van btw-functies.

### <a name="set-up-stores"></a>Winkels instellen

Werk op de pagina **Alle winkels** de winkeldetails bij. Stel met name de volgende parameters in.

- Geef in het veld **Btw-groep** de btw-groep op die moet wordenj gebruikt voor verkopen aan de standaardklant.
- Stel de optie **Prijzen zijn inclusief belasting** in op **Ja**.
- Stel het veld **Naam** in op de bedrijfsnaam. Door deze wijziging zorgt u ervoor dat de bedrijfsnaam op een ontvangstbewijs bij verkopen verschijnt. U kunt ook de bedrijfsnaam als vrije tekst aan de indeling voor ontvangstbewijzen voor verkopen toevoegen.
- Stel het veld **Btw-identificatienummer (TIN)** in op het bedrijfsidentificatienummer. Door deze wijziging zorgt u ervoor dat het identificatienummer van het bedrijf op een ontvangstbewijs bij verkopen verschijnt. U kunt ook het identificatienummer van het bedrijf als vrije tekst aan de indeling voor ontvangstbewijzen voor verkopen toevoegen.

### <a name="set-up-functionality-profiles"></a>Functionaliteitsprofielen instellen

POS-functionaliteitsprofielen instellen.

- Stel op het sneltabblad **Ontvangstbewijsnummering** in door records te maken of bij te werken voor de typen ontvangsttransacties **Verkoop**, **Verkooporder** en **Retour**.

### <a name="set-up-registration-numbers"></a>Registratienummers instellen

1. Ga naar **Organisatiebeheer \> Globaal adresboek \> Registratietypen \> Registratietypen**. Een nieuw registratietype maken. Stel het veld **Land/regio** in op **CZE** (Tsjechië) en beperk dit tot Organisatie.
2. Ga naar **Organisatiebeheer \> Globaal adresboek \> Registratietypen \> Registratiecategorieën**. Een nieuwe registratiecategorie maken. Selecteer het registratietype uit de vorige stap en stel de **registratiecategorie** in op **Bedrijfs-Id**.
3. Ga naar **Organisatiebeheer \> Organisaties \> Operationele eenheden**. Selecteer voor elke winkel in Tsjechië de eenheid die aan de winkel is gerelateerd. Vouw op het sneltabblad **Adres** de vervolgkeuzelijst **Meer opties** uit en selecteer vervolgens **Geavanceerd**. 
4. Op de pagina **Adressen beheren** moet u de volgende instellingen opgeven:

    - Stel op het sneltabblad **Adres** het veld **Land/regio** in op **CZE**.
    - Maak een nieuwe record op het sneltabblad **Registratie-id**. Selecteer het registratietype dat u eerder hebt gemaakt en stel het registratienummer in.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Aangepaste velden configureren zodat ze kunnen worden gebruikt in ontvangstbewijsindelingen

U kunt de taaltekst en aangepaste velden configureren die worden gebruikt in de POS-ontvangstindelingen. Het standaardbedrijf van de gebruiker die de ontvangstbewijsinstellingen maakt, moet dezelfde rechtspersoon zijn waar de taaltekstinstelling is gemaakt. Als alternatief moeten dezelfde taalteksten worden gemaakt in het standaardbedrijf van de gebruiker en in de rechtspersoon van de winkel waarvoor de instelling is gemaakt.

Voeg op de pagina **Taaltekst** de volgende records toe voor de labels van de aangepaste velden voor ontvangstbewijsindelingen. De waarden **Taal-id**, **Tekst-ID** en **Tekst** die in de tabel worden weergegeven, zijn slechts voorbeelden. U kunt ze eenvoudig wijzigen zodat ze aan uw behoeften voldoen. De waarden voor **Tekst-id** die u gebruikt, moeten echter uniek zijn en moeten gelijk zijn aan of groter zijn dan 900001.

Voeg de volgende POS-labels toe aan de sectie **POS** van **Taaltekst** uit de tabel:

| Taal-ID | Tekst-id | Tekst                   |
|-------------|---------|------------------------|
| nl       | 900001  | ID provozovny/pokladny |
| nl       | 900002  | BKP                    |
| nl       | 900003  | PKP                    |
| nl       | 900004  | FIK                    |
| nl       | 900005  | Info                   |
| nl       | 900006  | Volgnummer        |

Voeg op de pagina **Aangepaste velden** de volgende records toe voor de aangepaste velden voor ontvangstbewijsindelingen. Opmerking: waarden voor **Bijschrifttekst-id** moeten overeenkomen met de waarden voor **tekst-id's** die u hebt opgegeven op de pagina **Taaltekst**:

| Name                 | Type    | Tekst-id bijschrift |
|----------------------|---------|-----------------|
| TLT                  | Ontvangst | 900001          |
| SEC                  | Ontvangst | 900002          |
| SIGN                 | Ontvangst | 900003          |
| FISCAL               | Ontvangst | 900004          |
| INFO                 | Ontvangst | 900005          |
| CONTINUOUSNUMBER     | Ontvangst | 900006          |

> [!NOTE]
> Het is belangrijk dat u de juiste aangepaste veldnamen opgeeft, zoals aangegeven in de voorgaande tabel. Een onjuiste aangepaste veldnaam veroorzaakt ontbrekende gegevens in ontvangsten.

### <a name="configure-receipt-formats"></a>Indelingen voor ontvangstbewijzen configureren

Wijzig voor elke vereiste indeling voor ontvangstbewijzen de waarde van het veld **Afdrukgedrag** in **Altijd afdrukken**.

Voeg in de ontwerper van de ontvangstbewijsindeling de volgende aangepaste velden toe aan de juiste ontvangstbewijssecties. Opmerking: veldnamen komen overeen met de taalteksten die u in het vorige gedeelte hebt gedefinieerd.

- **Koptekst:** voeg de volgende velden toe.

    - **Winkelnaam** en **Btw-identiteitsnummer**: deze velden worden gebruikt om de bedrijfsnaam en het identiteitsnummer af te drukken op ontvangstbewijzen. U kunt ook de bedrijfsnaam en het identiteitsnummer als vrije tekst aan de indeling voor ontvangstbewijzen voor verkopen toevoegen.
    - **Winkeladres**, **Datum**, **Tijd 24 uur**, **Ontvangstbewijsnummer** en **Registernummer**.
    - **Volgnummer**: dit veld identificeert het nummer van de contante transactie in de fiscale registratieservice.

- **Regels:** voeg de volgende velden toe.

    - **Artikelnaam**
    - **Hoeveelheid**
    - **Totale prijs met btw**

- **Voettekst:** voeg de volgende velden toe.

    - Betalingsvelden zodat de betalingsbedragen voor elke betalingsmethode worden afgedrukt. Voeg bijvoorbeeld de velden **Naam van betalingsmethode** en **Bedrag van betalingsmethode** toe aan één regel van de indeling.
    - **ID provozovny/pokladny**: in dit veld worden de id's van het bedrijfsgebouw en de kassa afgedrukt.
    - **BKP**: dit veld drukt de beveiligingscode van de belastingbetaler af die door de fiscale registratieservice is toegewezen.
    - **FIK**: dit veld drukt de fiscale identificatiecode af van de transactie die is toegewezen door de webservice van de belastingdienst in geval van een geslaagde online registratie.
    - **PKP**: dit veld drukt de handtekeningcode van de belastingbetaler af die door de fiscale registratieservice wordt gegenereerd in het geval van offline registratie.
    - **Info**: dit veld drukt de extra informatie van de fiscale registratieservice af.

Zie [Ontvangstbewijsindelingen instellen en ontwerpen](../receipt-templates-printing.md) voor meer informatie over het werken met ontvangstbewijsindelingen.

## <a name="set-up-fiscal-integration-for-the-czech-republic"></a>Fiscale integratie voor Tsjechië instellen

Het voorbeeld van integratie van fiscale registratieservice voor Tsjechië is gebaseerd op de [functionaliteit voor fiscale integratie](fiscal-integration-for-retail-channel.md) en maakt deel uit van de Commerce SDK. Het voorbeeld bevindt zich in de map **src\\FiscalIntegration\\Efr** van de opslagplaats [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Het [voorbeeld](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) bestaat uit een fiscale documentprovider, hetgeen een extensie van de Commerce runtime (CRT) is, en een fiscale connector, die een uitbreiding is van Commerce Hardware Station. Voor meer informatie over het gebruik van de Commerce SDK, gaat u naar [Commerce SDK-voorbeelden en referentiepakketten van GitHub downloaden en NuGet](../dev-itpro/retail-sdk/sdk-github.md) en [Een build-pipeline instellen voor de onafhankelijke verpakkings-SDK](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Het voorbeeld van de belastingregistratieservice voor de Tsjechische Republiek is beschikbaar in de Commerce SDK vanaf Commerce versie 10.0.29. In Commercie versie 10.0.28 of eerder moet u de vorige versie van de Retail SDK gebruiken op een virtuele machine voor developers (VM) in Microsoft Dynamics Lifecycle Services (LCS). Zie [Implementatierichtlijnen voor het voorbeeld van fiscale integratie voor Tsjechië (verouderd)](emea-cze-fi-sample-sdk.md) voor meer informatie.

Voltooi de instellingsstappen voor de fiscale integratie zoals beschreven in [Fiscale integratie voor Commerce-kanalen instellen](setting-up-fiscal-integration-for-retail-channel.md):

1. [Een fiscaal registratieproces instellen](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Maak ook een notitie van de instellingen voor het fiscale registratieproces die [specifiek zijn voor dit voorbeeld van integratie van fiscale registratieservice](#set-up-the-registration-process).
1. [Instellingen voor het afhandelen van fouten uitvoeren](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).
1. [Handmatige uitvoering van uitgestelde fiscale registratie inschakelen](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-deferred-fiscal-registration).
1. [Kanaalonderdelen configureren](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Het fiscaal registratieproces instellen

Als u het registratieproces wilt inschakelen, voert u de volgende stappen uit om Commerce Headquarters in te stellen. Zie [De fiscale integratie voor Commerce-kanalen instellen](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process) voor meer informatie.

1. Download configuratiebestanden voor de fiscale documentprovider en de fiscale connector:

    1. Open de opslagplaats met [Dynamics 365 Commerce-oplossingen](https://github.com/microsoft/Dynamics365Commerce.Solutions/).
    1. Selecteer een juiste vertakkingsversie voor vrijgave volgens uw SDK/toepassingsversie.
    1. Open **src \> FiscalIntegration \> Efr**.
    1. Download het configuratiebestand van de fiscale documentprovider op **Configuraties \> DocumentProviders \> DocumentProviderFiscalEFRSampleCzech.xml**.
    1. Download het configuratiebestand van de fiscale connector via **Configuraties \> Connectors \> ConnectorEFRSample.xml**.

    > [!NOTE]
    > In Commercie versie 10.0.28 of eerder moet u de vorige versie van de Retail SDK gebruiken op een virtuele machine voor developers in LCS. De configuratiebestanden voor dit voorbeeld van fiscale integratie bevinden zich in de volgende mappen van de Retail SDK op een ontwikkelaars-VM in LCS:
    >
    > - **Configuratiebestand van fiscale documentprovider:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.EFRSample\\Configuration\\DocumentProviderFiscalEFRSampleCzech.xml
    > - **Configuratiebestand voor fiscale connector:** RetailSdk\\SampleExtensions\\HardwareStation\\Extension.EFRSample\\Configuration\\ConnectorEFRSample.xml

1. Ga naar **Detailhandel en commerce \> Instelling van hoofdkantoor \> Parameters \> Gedeelde Commerce-parameters**. Stel op het tabblad **Algemeen** de optie **Fiscale integratie inschakelen** in op **Ja**.
1. Ga naar **Retail en commerce \> Kanaalinstellingen \> Fiscale integratie \> Fiscale documentproviders** en laad het configuratiebestand voor de fiscale documentprovider die u eerder hebt gedownload.
1. Ga naar **Retail en commerce \> Kanaalinstellingen \> Fiscale integratie \> Fiscale connectors** en laad het configuratiebestand voor de fiscale connector die u eerder hebt gedownload.
1. Ga naar **Retail en Commerce \> Afzetkanaalinstellingen \> Fiscale integratie \> Functionele connectorprofielen**. Maak een nieuw functioneel connectorprofiel. Selecteer de documentprovider en de connector die u eerder hebt geladen. Werk de [instellingen voor gegevenstoewijzing](#default-data-mapping) bij waar nodig.
1. Ga naar **Retail en Commerce \> Afzetkanaalinstellingen \> Fiscale integratie \> Technische connectorprofielen**. Maak een nieuw technisch connectorprofiel en selecteer de fiscale connector die u eerder hebt geladen. Werk de [connectorinstellingen](#fiscal-connector-settings) bij waar nodig.
1. Ga naar **Retail en Commerce \> Afzetkanaalinstellingen \> Fiscale integratie \> Fiscale connectorgroepen**. Maak een nieuwe fiscale connectorgroep voor het functionele connectorprofiel dat u eerder hebt gemaakt.
1. Ga naar **Retail en Commerce \> Afzetkanaalinstellingen \> Fiscale integratie \> Fiscale registratieprocessen**. Maak een nieuw fiscaal registratieproces en een stap in het fiscale registratieproces en selecteer de fiscale connectorgroep die u eerder hebt gemaakt.
1. Ga naar **Retail en Commerce \> Kanaalinstellingen \> POS-instellingen \> POS-profielen \> Functionaliteitsprofielen**. Selecteer een functionaliteitsprofiel dat is gekoppeld aan de winkel waar het registratieproces moet worden geactiveerd. Selecteer op het sneltabblad **Fiscaal registratieproces** het fiscale registratieproces dat u eerder hebt gemaakt.
1. Ga naar **Retail en Commerce \> Kanaalinstellingen \> POS-instellingen \> POS-profielen \> Hardwareprofielen**. Selecteer een hardwareprofiel dat is gekoppeld aan het hardwarestation waarmee de fiscale registratieservice zal worden verbonden. Selecteer op het sneltabblad **Fiscale randapparatuur** het technische connectorprofiel dat u eerder hebt gemaakt.
1. Open de distributieplanning (**Retail en commerce \> Retail en commerce IT \> Distributieplanning**) en selecteer taken **1070** en **1090** om gegevens ovedr te dragen naar de kanaaldatabase.

#### <a name="default-data-mapping"></a>Standaardgegevenstoewijzing

De volgende standaardgegevenstoewijzing is opgenomen in de configuratie van de fiscale documentprovider die wordt opgegeven als onderdeel van het voorbeeld van fiscale integratie:

- **Btw-percentagetoewijzing**: de toewijzing van btw-percentagewaarden die voor de btw-codes worden ingesteld aan waarden van het kenmerk **TaxG** (btw-groep) in aanvragen die naar de fiscale service worden verzonden. Hier is de standaardtoewijzing:

    ```
    A: 21.00; B: 15.00; C: 10.00; Z: 0.00
    ```

    Het eerste onderdeel in elk koppel vertegenwoordigt een btw-groep die wordt ondersteund door de fiscale EFR-registratieservice. Het tweede onderdeel vertegenwoordigt het bijbehorende btw-tarief. Zie de [EFR-verwijzing](https://public.efsta.net/efr/) voor meer informatie over btw-groepen die EFR ondersteunt voor Tsjechië.

- **Standaard btw-groepstoewijzing**: alle btw-bedragen die niet kunnen worden toegewezen aan een van de vooraf bepaalde btw-groepen, worden toegeschreven aan de standaard (basis) btw-groep. Hier is de standaardtoewijzing:

    ```
    A
    ```

- **Toewijzing storting btw-groep:** stortingsbedragen van klanten en stortingsbedragen van klantorders worden toegeschreven aan de btw-groep voor stortingen. Hier is de standaardtoewijzing:

    ```
    Z
    ```

#### <a name="fiscal-connector-settings"></a>Instellingen voor fiscale connector

De volgende instellingen zijn opgenomen in de configuratie van de fiscale connector die wordt opgegeven als onderdeel van het voorbeeld van fiscale integratie:

- **Eindpuntadres**: de URL van de fiscale registratieservice.
- **Time-out**: de hoeveelheid tijd in milliseconden dat de fiscale connector wacht op een respons van de fiscale registratieservice.

### <a name="configure-channel-components"></a>Kanaalonderdelen configureren

> [!NOTE]
> - Het voorbeeld van de belastingregistratieservice voor de Tsjechische Republiek is beschikbaar in de Commerce SDK vanaf Commerce versie 10.0.29. In Commercie versie 10.0.28 of eerder moet u de vorige versie van de Retail SDK gebruiken op een virtuele machine voor developers in LCS. Zie [Implementatierichtlijnen voor het voorbeeld van fiscale integratie voor Tsjechië (verouderd)](emea-cze-fi-sample-sdk.md) voor meer informatie.
> - Voorbeelden voor Commerce die in uw omgeving worden geïmplementeerd, worden niet automatisch bijgewerkt wanneer u service- of kwaliteitsupdates toepast op Commerce-onderdelen. U moet de vereiste voorbeelden handmatig bijwerken.

#### <a name="set-up-the-development-environment"></a>De ontwikkelingsomgeving instellen

Voer de volgende stappen uit om een ontwikkelingsomgeving in te stellen zodat u het voorbeeld kunt testen en uitbreiden.

1. Kloon of download de [Dynamics 365 Commerce-oplossingen](https://github.com/microsoft/Dynamics365Commerce.Solutions). Selecteer een juiste vertakkingsversie voor vrijgave volgens uw SDK/toepassingsversie. Zie [Commerce SDK-voorbeelden en referentiepakketten van GitHub downloaden en NuGet](../dev-itpro/retail-sdk/sdk-github.md) voor meer informatie.
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

1. Uitbreidingen voor Fiscale connector installeren:

    U kunt uitbreidingen voor de fiscale connector installeren op het [hardwarestation](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-connected-to-the-hardware-station) of de [POS-kassa](fiscal-integration-for-retail-channel.md#fiscal-registration-is-done-via-a-device-or-service-in-the-local-network).

    1. Installeer extensies van Hardware Station:

        1. Zoek in de map **Efr\\HardwareStation\\HardwareStation.EFR.Installer\\bin\\Debug\\net461** het installatieprogramma **HardwareStation.EFR.Installer**.
        1. Start het installatieprogramma voor extensies vanaf de opdrachtregel door de volgende opdracht uit te voeren.

            ```Console
            HardwareStation.EFR.Installer.exe install --verbosity 0
            ```

    1. Installeer POS-extensies:

        1. Open de voorbeeldoplossing voor de POS fiscale connector op **Dynamics365Commerce.Solutions\\FiscalIntegration\\PosFiscalConnectorSample\\Contoso.PosFiscalConnectorSample.sln** en bouw deze.
        1. Zoek in de mpa **PosFiscalConnectorSample\\StoreCommerce.Installer\\bin\\Debug\\net461** het installatieprogramma **Contoso.PosFiscalConnectorSample.StoreCommerce.Installer**.
        1. Start het installatieprogramma voor extensies vanaf de opdrachtregel door de volgende opdracht uit te voeren.

            ```Console
            Contoso.PosFiscalConnectorSample.StoreCommerce.Installer.exe install --verbosity 0
            ```

#### <a name="production-environment"></a>Productieomgeving

Volg de stappen in [Een bouwpijplijn instellen voor een voorbeeld van fiscale integratie](fiscal-integration-sample-build-pipeline.md) voor het instellen en vrijgeven van de Cloud Scale Unit en selfservice implementeerbare pakketten voor het voorbeeld van fiscale integratie. Het YAML-sjabloonbestand **EFR build-pipeline.yml** is te vinden in de map **Pipeline\\YAML_Files** van de opslagplaats [Dynamics 365 Commerce-oplossingen](https://github.com/microsoft/Dynamics365Commerce.Solutions).

## <a name="design-of-extensions"></a>Ontwerp van extensies

Het voorbeeld van integratie van fiscale registratieservice voor Tsjechië is gebaseerd op de [functionaliteit voor fiscale integratie](fiscal-integration-for-retail-channel.md) en maakt deel uit van de Commerce SDK. Het voorbeeld bevindt zich in de map **src\\FiscalIntegration\\Efr** van de opslagplaats [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Het [voorbeeld](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) bestaat uit een fiscale documentprovider, die een extensie van CRT is, en een fiscale connector, die een extensie is van Commerce Hardware Station. Voor meer informatie over het gebruik van de Commerce SDK, gaat u naar [Commerce SDK-voorbeelden en referentiepakketten van GitHub downloaden en NuGet](../dev-itpro/retail-sdk/retail-sdk-overview.md) en [Een build-pipeline instellen voor de onafhankelijke verpakkings-SDK](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Het voorbeeld van de belastingregistratieservice voor de Tsjechische Republiek is beschikbaar in de Commerce SDK vanaf Commerce versie 10.0.29. In Commercie versie 10.0.28 of eerder moet u de vorige versie van de Retail SDK gebruiken op een virtuele machine voor developers in LCS. Zie [Implementatierichtlijnen voor het voorbeeld van fiscale integratie voor Tsjechië (verouderd)](emea-cze-fi-sample-sdk.md) voor meer informatie.

### <a name="commerce-runtime-extension-design"></a>Ontwerp van Commerce runtime-extensie

De extensie die een fiscale documentprovider is, heeft tot doel om servicespecifieke documenten te genereren en responsen van de fiscale registratieservice af te handelen.

#### <a name="request-handler"></a>Aanvraaghandler

Er is een enkele aanvraaghandler **DocumentProviderEFRFiscalCZE** voor documentproviders, die wordt gebruikt om fiscale documenten te genereren voor de fiscale registratieservice.

Deze handler wordt overgenomen van de interface **INamedRequestHandler**. De methode **HandlerName** is verantwoordelijk voor het retourneren van de naam van de handler. De handlernaam moet overeenkomen met de naam van de connector-documentprovider die is opgegeven in Commerce Headquarters.

De connector ondersteunt de volgende aanvragen.

- **GetFiscalDocumentDocumentProviderRequest**: deze aanvraag bevat informatie over welk document moet worden gegenereerd. Het retourneert een servicespecifieke document dat in de fiscale registratieservice moet worden geregistreerd.
- **GetSupportedRegistrableEventsDocumentProviderRequest**: met deze aanvraag retourneert u de lijst met gebeurtenissen waarop u een abonnement wilt nemen. Op dit moment worden de volgende gebeurtenissen ondersteund: verkoop, klantaccountstortingen en klantorderstortingen.
- **GetFiscalRegisterResponseToSaveDocumentProviderRequest:** met deze aanvraag wordt het antwoord van de fiscale registratieservice geretourneerd. Dit antwoord wordt geseraliseerd om een tekenreeks te vormen zodat deze gereed is om te worden opgeslagen.

#### <a name="configuration"></a>Configuratie

Het configuratiebestand voor de fiscale documentprovider bevindt zich in **src\\FiscalIntegration\\Efr\\Configurations\\DocumentProviders\\DocumentProviderFiscalEFRSampleCzech.xml** in de opslagplaats [Dynamics 365 Commerce-oplossingen](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Het doel van het bestand is het inschakelen van instellingen van de fiscale documentprovider die moeten worden geconfigureerd vanuit Commerce Headquarters. De bestandsindeling is afgestemd op de vereisten voor de configuratie van fiscale integratie.

### <a name="hardware-station-extension-design"></a>Ontwerp van extensies voor hardwarestation

De extensie die een fiscale connector is, heeft tot doel om te communiceren met de fiscale registratieservice. De hardwarestationextensie gebruikt het HTTP-protocol om documenten die de CRT-extensie genereert in te dienen bij de fiscale registratieservice. Het verwerkt ook de responsen die van de fiscale registratieservice worden ontvangen.

#### <a name="request-handler"></a>Aanvraaghandler

De aanvraaghandler **EFRHandler** is het invoerpunt voor het afhandelen van aanvragen bij de fiscale registratieservice.

De handler wordt overgenomen van de interface **INamedRequestHandler**. De methode **HandlerName** is verantwoordelijk voor het retourneren van de naam van de handler. De handlernaam moet overeenkomen met de naam van de fiscale connector die is opgegeven in Commerce Headquarters.

De connector ondersteunt de volgende aanvragen.

- **SubmitDocumentFiscalDeviceRequest**: met deze aanvraag worden documenten naar de fiscale registratieservice verzonden en wordt hierop een respons geretourneerd.
- **IsReadyFiscalDeviceRequest**: deze aanvraag wordt gebruikt voor een statuscontrole van de fiscale registratieservice.
- **InitializeFiscalDeviceRequest**: deze aanvraag wordt gebruikt om de fiscale registratieservice te initialiseren.

#### <a name="configuration"></a>Configuratie

Het configuratiebestand voor de fiscale connector bevindt zich op **src\\FiscalIntegration\\Efr\\Configurations\\Connectors\\ConnectorEFRSample.xml** in de opslagplaats voor [Dynamics 365 Commerce-oplossingen](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Het doel van het bestand is het inschakelen van instellingen van de fiscale connector die moet worden geconfigureerd vanuit Commerce Headquarters. De bestandsindeling is afgestemd op de vereisten voor de configuratie van fiscale integratie.

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

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
