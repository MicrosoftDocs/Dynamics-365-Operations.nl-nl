---
title: Voorbeeld van integratie van fiscale registratieservice voor Duitsland
description: Dit artikel biedt een overzicht van het fiscale integratievoorbeeld voor Duitsland in Microsoft Dynamics 365 Commerce.
author: EvgenyPopovMBS
ms.date: 10/04/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2020-05-29
ms.openlocfilehash: a725badbce498e4e7b35aecb2500e273586c7b77
ms.sourcegitcommit: 2bc6680dc6b12d20532d383a0edb84d180885b62
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/06/2022
ms.locfileid: "9631448"
---
# <a name="fiscal-registration-service-integration-sample-for-germany"></a>Voorbeeld van integratie van fiscale registratieservice voor Duitsland

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Dit artikel biedt een overzicht van het fiscale integratievoorbeeld voor Duitsland in Microsoft Dynamics 365 Commerce.

Als u wilt voldoen aan de lokale fiscale vereisten voor kassa's in Duitsland, omvat de Dynamics 365 Commerce-functionaliteit voor Duitsland een voorbeeldintegratie van het POS (point-of-sale) met een externe fiscale registratieservice. In het voorbeeld wordt de [functionaliteit voor fiscale integratie](fiscal-integration-for-retail-channel.md) uitgebreid. Het is gebaseerd op de [EFR-oplossing (Electronic Fiscal Register)](https://www.efsta.eu/de/fiskalloesungen/deutschland) van [EFSTA](https://www.efsta.eu/de/) en maakt communicatie met de EFR-service via het HTTPS-protocol mogelijk. De EFR-service moet worden gehost op het retailhardwarestation of op een afzonderlijke computer waarmee verbinding kan worden gemaakt vanuit het hardwarestation. Het voorbeeld wordt geleverd in de vorm van broncode en maakt deel uit van de Commerce Software Development Kit (SDK).

Microsoft brengt geen hardware, software of documentatie van EFSTA uit. Neem contact op met [EFSTA](https://www.efsta.eu/de/kontakt/kontakt) voor informatie over het verkrijgen van de EFR-oplossing en de werking ervan.

## <a name="scenarios"></a>Scenario's

De volgende scenario's worden gedekt door het voorbeeld van de integratie van een fiscale registratieservice voor Duitsland:

### <a name="sales-operations"></a>Verkoopbewerkingen

- **Registratie van contante verkooptransacties en retouren met contant geld in de fiscale registratieservice:**

    Registratie van verkoopbewerkingen omvat de volgende stappen:

    1. Registratie van het begin van de transactie

        Het begin van elke transactie wordt geregistreerd in een technisch beveiligingselement (TSE) dat met de EFR-service is verbonden. Als gevolg van de registratie, wijst een TSE een transactie-id (TID) toe.

    2. Registratie van het einde van de transactie

        Wanneer er een transactie wordt gemaakt op het POS, wordt deze geregistreerd met dezelfde TID die is toegewezen tijdens de registratie van het begin van de transactie. Op dat moment worden gedetailleerde transactiegegevens naar de fiscale registratieservice verzonden. Deze gegevens bevatten verkoopregelgegevens en informatie over kortingen, betalingen en btw.

    3. Een respons van de fiscale registratieservice vastleggen

        Beveiligingsgegevens worden als onderdeel van een respons van een TSE ontvangen en worden opgeslagen in de transactie in de kanaaldatabase. De beveiligingsgegevens bestaan uit de volgende informatie:

        - TID
        - Datum en tijdstip van het begin van de transactie
        - Datum en tijdstip van het einde van de transactie
        - Handtekeningteller
        - Controlewaarde
        - Serienummer van de TSE

- **Registratie van klantorders in de fiscale registratieservice:** het registratieproces is hetzelfde als het proces voor contante verkooptransacties en retouren.
- **Registratie van bewerkingen met betrekking tot geschenkbonnen en stortingen:** het registratieproces is hetzelfde als het proces voor contante verkooptransacties en retouren.

#### <a name="notifying-users-about-fiscal-registration-failures"></a>Gebruikers op de hoogte stellen van fouten in fiscale registraties

Er zijn twee manieren waarop de fiscale registratieservice gebruikers op de hoogte kan stellen van fouten die zich hebben voorgedaan tijdens de fiscale registratie:

- Druk extra informatie over de respons af in het veld **Informatiebericht** op ontvangstbewijzen.
- Geef meldingen van de fiscale service weer als gebruikersberichten op het POS.

    > [!NOTE]
    > Voor dit meldingsmechanisme moet de parameter **Meldingen fiscale registratie weergeven** op de pagina **Technische connectorprofielen** worden ingeschakeld.

#### <a name="printing-receipts"></a>Ontvangstbewijzen afdrukken

Het afdrukken van ontvangstbewijzen is verplicht in Duitsland. Alle ontvangstbewijzen moeten ten minste de volgende gegevens bevatten:

- Naam en adres van het bedrijf
- Informatie over goederen, waaronder de prijzen en hoeveelheden
- Informatie over ontvangen betalingen
- Informatie over belastingen, waaronder totaalbedragen per btw-tarief
- Beveiligingsgegevens:

    - TID
    - Datum en tijdstip van het begin van de transactie
    - Datum en tijdstip van het einde van de transactie
    - Handtekeningteller
    - Controlewaarde
    - Serienummer van de TSE

- Informatief bericht

> [!NOTE]
> Op ontvangstbewijzen kan ook een QR-code worden afgedrukt. Hoewel de QR-code optioneel is, wordt deze sterk aanbevolen. Zie het document 'EFR Guide \[DE\]' dat wordt gepubliceerd op de [EFSTA-documentatiewebsite](https://public.efsta.net/efr/) voor meer informatie over het ophalen van een QR-code als onderdeel van een respons van de fiscale registratieservice.
>
> In het veld **Informatiebericht** op ontvangstbewijzen wordt een melding van de fiscale registratieservice weergegeven. Als bijvoorbeeld een handtekeningapparaat stuk is, kan er speciale tekst worden afgedrukt op een ontvangstbewijs.

#### <a name="voided-suspended-and-recalled-transactions"></a>Ongeldig gemaakte, uitgestelde en teruggeroepen transacties

- Een ongeldig gemaakte transactie wordt geregistreerd als een aanvraag om een transactie in de fiscale registratieservice te beëindigen.
- Een uitgestelde transactie wordt geregistreerd als een aanvraag om een transactie in de fiscale registratieservice te beëindigen.
- Het terugroepen van een uitgestelde transactie wordt geregistreerd als het begin van een nieuwe transactie in de fiscale registratieservice.

### <a name="non-sales-transactions-and-shift-closing"></a>Niet-verkooptransacties en sluiting van ploegen

De volgende niet-verkooptransacties worden geregistreerd als niet-fiscale bewerkingen in de fiscale registratieservice met het label **NFS**:

- Beginbedrag declareren
- Wisselgeldinvoer
- Wisselgeld verwijderen
- Kluisstorting
- Bankstorting
- Inkomstenrekeningen
- Uitgavenrekeningen

De bewerking **Ploeg sluiten** wordt eveneens geregistreerd als niet-fiscale bewerking in de fiscale registratieservice met het label **NFS**.

### <a name="data-export-and-audit"></a>Gegevensexport en -controle

Alle transacties moeten door een TSE worden ondertekend om hun integriteit, echtheid en volledigheid te garanderen en om te voorkomen dat geregistreerde gegevens worden bewerkt.

> [!WARNING]
> Alleen een gecertificeerde TSE kan worden gebruikt. Zie het document "EFR Guide \[DE\]"dat wordt gepubliceerd op de [EFSTA-documentatiewebsite](https://public.efsta.net/efr/) voor informatie over de typen en modellen van TSE's die worden ondersteund in de EFR-oplossing. Neem contact op met [EFSTA](https://www.efsta.eu/at/kontakt) voor informatie over het kiezen en verkrijgen van een TSE.

De regelgeving in Duitsland vereist ondersteuning voor de DSFinV-K-export. De DSFinV-K-export kan worden geactiveerd in de EFR-oplossing. Zie het document "EFR Guide \[DE\]" dat wordt gepubliceerd op de [EFSTA-documentatiewebsite](https://public.efsta.net/efr/) voor meer informatie over de DSFinV-K-export.

### <a name="limitations-of-the-sample"></a>Beperkingen van het voorbeeld

De fiscale registratieservice ondersteunt alleen scenario's waarin prijzen inclusief btw zijn. Daarom moet de optie **Prijzen inclusief btw** zijn ingesteld op **Ja** voor zowel winkels als klanten.

De fiscale service biedt geen ondersteuning voor situaties waarin meerdere btw-codes op dezelfde transactieregel worden toegepast.

Het fiscale integratieraamwerk ondersteunt geen verkoopoffertes. Deze bewerkingen zijn daarom niet in de fiscale service geregistreerd.

## <a name="set-up-commerce-for-germany"></a>Commerce instellen voor Duitsland

In deze sectie worden de Commerce-instellingen beschreven die specifiek en aanbevolen zijn voor Duitsland. Zie [Startpagina voor Commerce](../index.md) voor meer instellingsinformatie.

Als u de functionaliteit die specifiek is voor Duitsland wilt gebruiken, moet u de volgende instellingen opgeven.

- Stel in het primaire adres van de rechtspersoon het veld **Land/regio** in op **DEU** (Duitsland).
- Stel in het POS-functionaliteitsprofiel van elke winkel die zich in Duitsland bevindt het veld **ISO-code** in op **DE** (Duitsland).

U moet ook de volgende instellingen opgeven voor Duitsland. Voer de juiste distributietaken uit nadat u de instellingen hebt voltooid.

### <a name="set-up-vat-per-german-requirements"></a>Btw instellen volgens de Duitse vereisten

U moet btw-codes, btw-groepen en btw-groepen voor artikelen maken. U moet ook btw-gegevens instellen voor producten en services. Zie [Btw-overzicht](../../finance/general-ledger/indirect-taxes-overview.md) voor meer informatie over het instellen en gebruiken van btw-functies.

Op ontvangstbewijzen bij verkopen kunt u een afgekorte code afdrukken voor een btw-code (bijvoorbeeld "A" of "B"). Stel deze functionaliteit beschikbaar door het veld **Code afdrukken** in te stellen op de pagina **Btw-codes**.

### <a name="set-up-stores"></a>Winkels instellen

Werk op de pagina **Alle winkels** de winkeldetails bij. Stel met name de volgende parameters in:

- Geef in het veld **Btw-groep** de btw-groep op die moet wordenj gebruikt voor verkopen aan de standaardklant.
- Stel de optie **Prijzen zijn inclusief belasting** in op **Ja**.
- Stel het veld **Naam** in op de bedrijfsnaam. Door deze wijziging zorgt u ervoor dat de bedrijfsnaam op een ontvangstbewijs bij verkopen verschijnt. U kunt ook de bedrijfsnaam als vrije tekst aan de indeling voor ontvangstbewijzen voor verkopen toevoegen.
- Stel het veld **Btw-identificatienummer (TIN)** in op het bedrijfsidentificatienummer. Door deze wijziging zorgt u ervoor dat het identificatienummer van het bedrijf op een ontvangstbewijs bij verkopen verschijnt. U kunt ook het identificatienummer van het bedrijf als vrije tekst aan de indeling voor ontvangstbewijzen voor verkopen toevoegen.

### <a name="set-up-functionality-profiles"></a>Functionaliteitsprofielen instellen

POS-functionaliteitsprofielen instellen. Stel op het sneltabblad **Ontvangstbewijsnummering** in door records te maken of bij te werken voor de typen ontvangsttransacties **Verkoop**, **Verkooporder** en **Retour**.

### <a name="configure-custom-fields-so-that-they-can-be-used-in-receipt-formats-for-sales-receipts"></a>Aangepaste velden configureren zodat ze kunnen worden gebruikt in ontvangstbewijsindelingen

U kunt de taaltekst en aangepaste velden configureren die worden gebruikt in de POS-ontvangstindelingen. Het standaardbedrijf van de gebruiker die de ontvangstbewijsinstellingen maakt, moet dezelfde rechtspersoon zijn waar de taaltekstinstelling is gemaakt. Als alternatief moeten dezelfde taalteksten worden gemaakt in het standaardbedrijf van de gebruiker en in de rechtspersoon van de winkel waarvoor de instelling is gemaakt.

Voeg op de pagina **Taaltekst** de volgende records toe voor de labels van de aangepaste velden voor ontvangstbewijsindelingen. De waarden **Taal-id**, **Tekst-ID** en **Tekst** die in de tabel worden weergegeven, zijn slechts voorbeelden. U kunt ze eenvoudig wijzigen zodat ze aan uw behoeften voldoen. De waarden voor **Tekst-id** die u gebruikt, moeten echter uniek zijn en moeten gelijk zijn aan of groter zijn dan 900001.

Voeg de volgende POS-labels toe aan de sectie **POS** van de pagina **Taaltekst**.

| Taal-ID | Tekst-id | Tekst                                  |
|-------------|---------|---------------------------------------|
| nl       | 900001  | QR-code                               |
| nl       | 900002  | Transactie-ID                        |
| nl       | 900003  | Afdrukcode btw-detailhandel                 |
| nl       | 900004  | Btw-bedrag (verkopen)                    |
| nl       | 900005  | Btw-basis (verkopen)                     |
| nl       | 900006  | Begindatum/-tijd van transactie           |
| nl       | 900007  | Einddatum/-tijd van transactie             |
| nl       | 900008  | Serienummer van het beveiligingselement |
| nl       | 900009  | Handtekeningteller                     |
| nl       | 900010  | Controlewaarde                           |
| nl       | 900011  | Informatiebericht                          |

Voeg op de pagina **Aangepaste velden** de volgende records toe voor de aangepaste velden voor ontvangstbewijsindelingen. Opmerking: de waarden voor **Bijschrifttekst-id** moeten overeenkomen met de waarden voor **tekst-id's** die u hebt opgegeven op de pagina **Taaltekst**.

| Name                            | Type    | Tekst-id bijschrift |
|---------------------------------|---------|-----------------|
| QRCODE\_DE                      | Ontvangst | 900001          |
| TRANSACTIONID\_DE               | Ontvangst | 900002          |
| RETAILPRINTCODE\_DE             | Ontvangst | 900003          |
| SALESTAXAMOUNT\_DE              | Ontvangst | 900004          |
| SALESTAXBASIS\_DE               | Ontvangst | 900005          |
| TRANSACTIONSTARTDATETIME\_DE    | Ontvangst | 900006          |
| TRANSACTIONENDDATETIME\_DE      | Ontvangst | 900007          |
| SECURITYELEMENTSERIALNUMBER\_DE | Ontvangst | 900008          |
| SIGNCOUNTER\_DE                 | Ontvangst | 900009          |
| SIGN\_DE                        | Ontvangst | 900010          |
| INFOMESSAGE\_DE                 | Ontvangst | 900011          |

> [!NOTE]
> Het is belangrijk dat u de juiste aangepaste veldnamen opgeeft, zoals aangegeven in de voorgaande tabel. Een onjuiste aangepaste veldnaam veroorzaakt ontbrekende gegevens in ontvangsten.

### <a name="configure-receipt-formats"></a>Indelingen voor ontvangstbewijzen configureren

Wijzig voor elke indeling die is vereist voor ontvangstbewijzen de waarde van het veld **Afdrukgedrag** in **Altijd afdrukken**.

Voeg in de ontwerper van de ontvangstbewijsindeling de volgende aangepaste velden toe aan de juiste ontvangstbewijssecties. Opmerking: veldnamen komen overeen met de taalteksten die u in het vorige gedeelte hebt gedefinieerd.

- **Koptekst:** voeg de volgende velden toe:

    - Velden **Winkelnaam** en **Btw-identiteitsnummer** die worden gebruikt om de bedrijfsnaam en het identificatienummer af te drukken op ontvangstbewijzen. U kunt ook de bedrijfsnaam en het identificatienummer als vrije tekst aan de indeling voor ontvangstbewijzen voor verkopen toevoegen.
    - Velden **Winkeladres**, **Datum**, **Tijd 24 uur**, **Ontvangstbewijsnummer** en **Registernummer**.

- **Regels:** voeg de volgende velden toe:

    - Veld **Artikelnaam**
    - Veld **Hoev.**
    - Veld **Totale prijs met btw**
    - Veld **Afdrukcode btw-detailhandel**, waarmee de afgekorte code wordt afgedrukt die overeenkomt met de btw-code die geldt voor het artikel

- **Voettekst:** voeg de volgende velden toe:

    - Betalingsvelden zodat de betalingsbedragen voor elke betalingsmethode worden afgedrukt. Voeg bijvoorbeeld de velden **Naam van betalingsmethode** en **Bedrag van betalingsmethode** toe aan één regel van de indeling.
    - Velden in de veldgroep **Btw-opsplitsing**. Alle velden in deze veldgroep moeten op één afzonderlijke regel worden afgedrukt.

        - Veld **Btw-id**, dat een standaardveld is waarmee voor elke btw-code een btw-overzicht kan worden afgedrukt. Het veld moet worden toegevoegd aan een nieuwe regel.
        - Veld **Btw-percentage**, dat een standaardveld is dat wordt gebruikt om het effectieve btw-percentage voor de btw-code af te drukken.
        - Veld **Btw-basis (verkopen)**, dat wordt gebruikt om het totale bedrag aan contante verkopen voor de btw-code af te drukken. Vooruitbetalingen en bewerkingen voor geschenkbonnen zijn uitgesloten.
        - Veld **Btw-bedrag (verkopen)**, dat wordt gebruikt om het totale bedrag voor contante verkopen voor de btw-code op het ontvangstbewijs af te drukken.
        - Veld **Afdrukcode btw-detailhandel**, waarmee de afgekorte code wordt afgedrukt die overeenkomt met de btw-code.

    - Velden met beveiligde transactiegegevens die door de fiscale registratieservice worden geretourneerd:

        - Veld **Transactie-id**, voor het identificeren van het nummer van de contante transactie in de fiscale registratieservice
        - Veld **Begindatum van transactie**
        - Veld **Einddatum van transactie**
        - Veld **Serienummer van het beveiligingselement**
        - Veld **Handtekeningteller**
        - Veld **Controlewaarde**
        - Veld **QR-code**, dat wordt gebruikt om de verwijzing naar de geregistreerde contante transactie af te drukken in de vorm van een QR-code

        > [!NOTE]
        > De waarde **QR-code** wordt opgehaald uit het antwoord van het fiscale register. EFR retourneert alleen een QR-code als de waarde van het veld **Kenmerken** in de EFR-configuratie is beschreven in de EFSTA-documentatie. De notatie van de QR-code in het veld **Kenmerken** in de EFR-configuratie moet worden ingesteld op **BMP**.

    - Veld **Informatiebericht**, voor het weergeven van meldingsberichten van de fiscale registratieservice op ontvangstbewijzen. Als bijvoorbeeld een handtekeningapparaat stuk is, kan er speciale tekst worden afgedrukt op een ontvangstbewijs.

Zie [Ontvangstbewijsindelingen instellen en ontwerpen](../receipt-templates-printing.md) voor meer informatie over het werken met ontvangstbewijsindelingen.

## <a name="set-up-fiscal-integration-for-germany"></a>Fiscale integratie instellen voor Duitsland

Het voorbeeld van integratie van fiscale registratieservice voor Duitsland is gebaseerd op de [functionaliteit voor fiscale integratie](fiscal-integration-for-retail-channel.md) en maakt deel uit van de Commerce SDK. Het voorbeeld bevindt zich in de map **src\\FiscalIntegration\\Efr** van de opslagplaats [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Het [voorbeeld](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) bestaat uit een fiscale documentprovider, hetgeen een extensie van de Commerce runtime (CRT) is, en een fiscale connector, die een uitbreiding is van Commerce Hardware Station. Voor meer informatie over het gebruik van de Commerce SDK, gaat u naar [Commerce SDK-voorbeelden en referentiepakketten van GitHub downloaden en NuGet](../dev-itpro/retail-sdk/sdk-github.md) en [Een build-pipeline instellen voor de onafhankelijke verpakkings-SDK](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Het voorbeeld van de belastingregistratieservice voor Duitsland is beschikbaar in de Commerce SDK vanaf Commerce versie 10.0.29. In Commercie versie 10.0.28 of eerder moet u de vorige versie van de Retail SDK gebruiken op een virtuele machine voor developers (VM) in Microsoft Dynamics Lifecycle Services (LCS). Zie [Implementatierichtlijnen voor het voorbeeld van fiscale integratie voor Duitsland (verouderd)](emea-deu-fi-sample-sdk.md) voor meer informatie.

Voltooi de instellingsstappen voor de fiscale integratie zoals beschreven in [Fiscale integratie voor Commerce-kanalen instellen](setting-up-fiscal-integration-for-retail-channel.md):

1. [Een fiscaal registratieproces instellen](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process). Maak ook een notitie van de instellingen voor het fiscale registratieproces die [specifiek zijn voor dit voorbeeld van integratie van fiscale registratieservice](#set-up-the-registration-process).
1. [Instellingen voor het afhandelen van fouten uitvoeren](setting-up-fiscal-integration-for-retail-channel.md#set-error-handling-settings).

    > [!WARNING]
    > De mogelijkheden voor het verwerken van fouten van het fiscale integratieraamwerk zijn mogelijk niet volledig afgestemd op de lokale belastingregels.
    >
    > - Het wordt aangeraden de optie **Doorgaan bij fout** op de pagina **Fiscaal registratieproces** uit te schakelen, omdat alle transacties juist moeten worden geregistreerd, zelfs als de eerste poging tot belastingregistratie is mislukt.
    > - Voordat u de optie **Overslaan** of **Markeren als geregistreerd** inschakelt op de pagina **Fiscaal registratieproces**, moet u deze wijzigingen in het fiscale registratieproces bespreken met uw belastingconsultant of het lokale belastingkantoor.

1. [Handmatige uitvoering van uitgestelde fiscale registratie inschakelen](setting-up-fiscal-integration-for-retail-channel.md#enable-manual-execution-of-deferred-fiscal-registration).
1. [Kanaalonderdelen configureren](#configure-channel-components).

### <a name="set-up-the-registration-process"></a>Het fiscaal registratieproces instellen

Als u het registratieproces wilt inschakelen, voert u de volgende stappen uit om Commerce Headquarters in te stellen. Zie [De fiscale integratie voor Commerce-kanalen instellen](setting-up-fiscal-integration-for-retail-channel.md#set-up-a-fiscal-registration-process) voor meer informatie.

1. Download configuratiebestanden voor de fiscale documentprovider en de fiscale connector:

    1. Open de opslagplaats met [Dynamics 365 Commerce-oplossingen](https://github.com/microsoft/Dynamics365Commerce.Solutions/).
    1. Selecteer een juiste vertakkingsversie voor vrijgave volgens uw SDK/toepassingsversie.
    1. Open **src \> FiscalIntegration \> Efr**.
    1. Download het configuratiebestand van de fiscale documentprovider op **Configuraties \> DocumentProviders \> DocumentProviderFiscalEFRSampleGermany.xml**.
    1. Download het configuratiebestand van de fiscale connector via **Configuraties \> Connectors \> ConnectorEFRSample.xml**.

    > [!NOTE]
    > In Commercie versie 10.0.28 of eerder moet u de vorige versie van de Retail SDK gebruiken op een virtuele machine voor developers in LCS. De configuratiebestanden voor dit voorbeeld van fiscale integratie bevinden zich in de volgende mappen van de Retail SDK op een ontwikkelaars-VM in LCS:
    >
    > - **Configuratiebestand van fiscale documentprovider:** RetailSdk\\SampleExtensions\\CommerceRuntime\\Extensions.DocumentProvider.EFRSample\\Configuration\\DocumentProviderFiscalEFRSampleGermany.xml
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

- **Toewijzing betalingsmethode**: de toewijzing van betalingsmethoden aan waarden van het kenmerk **PayG** (betalingsgroep) in aanvragen die naar de fiscale service worden verzonden. Hier is de standaardtoewijzing:

    ```
    1: 0; 2: 1; 3: 3; 4: 8; 5: 2; 6: 0; 7: 7; 8: 6; 9: 0; 10: 8; 11: 1
    ```

    Het eerste onderdeel in elk koppel vertegenwoordigt een betalingsmethode die is ingesteld voor de winkel. Het tweede onderdeel vertegenwoordigt de bijbehorende betalingsgroep die wordt ondersteund door de fiscale EFR-registratieservice. Zie de [EFR-verwijzing](https://public.efsta.net/efr/) voor meer informatie over betalingsgroepen die EFR ondersteunt voor Duitsland.

    De voorbeeldtoewijzing van betalingsmethoden komt overeen met de winkelbetalingsmethoden die zijn geconfigureerd in de standaarddemogegevens.

    | Betaalwijze | Naam betalingsmethode |
    |----------------|---------------------|
    | 1              | Contant                |
    | 2              | Controleren               |
    | 3              | Kaart                |
    | 4              | Klantrekening    |
    | 5              | Anders               |
    | 6              | Valuta            |
    | 7              | Boekstuk             |
    | 8              | Geschenkbon           |
    | 9              | Betalingsmethode verwijderen/wisselgeld |
    | 10             | Loyaliteitskaarten       |
    | 11             | Niet-lokale controles    |

    Daarom moet u de voorbeeldtoewijzing wijzigen volgens de betalingsmethoden die in de toepassing zijn geconfigureerd.

- **Klantgegevens opnemen**: als deze parameter is ingeschakeld, bevatten aanvragen voor de fiscale service klantgegevens, zoals namen en adressen, wanneer een klant aan een transactie wordt toegevoegd.
- **Btw-percentagetoewijzing**: de toewijzing van btw-percentagewaarden die voor de btw-codes worden ingesteld aan waarden van het kenmerk **TaxG** (btw-groep) in aanvragen die naar de fiscale service worden verzonden. Hier is de standaardtoewijzing:

    ```
    A: 19.00; B: 7.00; C: 10.70; D: 5.50; E: 0.00
    ```

    Het eerste onderdeel in elk koppel vertegenwoordigt een btw-groep die wordt ondersteund door de fiscale EFR-registratieservice. Het tweede onderdeel vertegenwoordigt het bijbehorende btw-tarief. Zie de [EFR-verwijzing](https://public.efsta.net/efr/) voor meer informatie over btw-groepen die EFR ondersteunt voor Duitsland.

- **Btw-groep voor geschenkaanvragen en stortingen:** de waarde van het kenmerk **TaxG** in aanvragen die naar de fiscale service worden verzonden, op basis van bewerkingen waarbij geschenkaanvragen of stortingen zijn betrokken. Hier is de standaardtoewijzing:

    ```
    G
    ```

- **Btw-groep voor btw-vrijstelling:** de waarde van het kenmerk **TaxG** in aanvragen die naar de fiscale service worden verzonden op basis van bewerkingen die zijn vrijgesteld van belastingverplichtingen. Hier is de standaardtoewijzing:

    ```
    F
    ```

> [!NOTE]
> Btw-instellingen in de standaardgegevenstoewijzing zijn verantwoordelijk voor overeenkomende btw-instellingen in het systeem en de btw-groepen in de EFR-service. Btw-groepen kunnen alleen op ontvangstbewijzen worden afgedrukt als het veld **Code voor afdrukken** is ingesteld op de pagina **Btw-codes**.

#### <a name="fiscal-connector-settings"></a>Instellingen voor fiscale connector

De volgende instellingen zijn opgenomen in de configuratie van de fiscale connector die wordt opgegeven als onderdeel van het voorbeeld van fiscale integratie:

- **Eindpuntadres**: de URL van de fiscale registratieservice.
- **Time-out**: de hoeveelheid tijd in milliseconden dat de fiscale connector wacht op een respons van de fiscale registratieservice.
- **Meldingen fiscale registratie weergeven**: met deze vlag wordt bepaald of meldingen die worden weergegeven aan de operator voor de fiscale registratieservice moeten worden weergegeven.

### <a name="configure-channel-components"></a>Kanaalonderdelen configureren

> [!NOTE]
> - Het voorbeeld van de belastingregistratieservice voor Duitsland is beschikbaar in de Commerce SDK vanaf Commerce versie 10.0.29. In Commercie versie 10.0.28 of eerder moet u de vorige versie van de Retail SDK gebruiken op een virtuele machine voor developers in LCS. Zie [Implementatierichtlijnen voor het voorbeeld van fiscale integratie voor Duitsland (verouderd)](emea-deu-fi-sample-sdk.md) voor meer informatie.
> - Voorbeelden voor Commerce die in uw omgeving worden geïmplementeerd, worden niet automatisch bijgewerkt wanneer u service- of kwaliteitsupdates toepast op Commerce-onderdelen. U moet de vereiste voorbeelden handmatig bijwerken.

#### <a name="set-up-the-development-environment"></a>De ontwikkelingsomgeving instellen

Voer de volgende stappen uit om een ontwikkelingsomgeving in te stellen zodat u het voorbeeld kunt testen en uitbreiden.

1. Kloon of download de [Dynamics 365 Commerce-oplossingen](https://github.com/microsoft/Dynamics365Commerce.Solutions). Selecteer een juiste vertakkingsversie voor vrijgave volgens uw SDK/toepassingsversie. Zie [Commerce SDK-voorbeelden en referentiepakketten van GitHub downloaden en NuGet](../dev-itpro/retail-sdk/sdk-github.md) voor meer informatie.
1. Open de EFR-oplossing op **Dynamics365Commerce.Solutions\\FiscalIntegration\\Efr\\EFR.sln** en bouw deze.
1. Commerce Runtime-extensies installeren:

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

Het voorbeeld van integratie van fiscale registratieservice voor Duitsland is gebaseerd op de [functionaliteit voor fiscale integratie](fiscal-integration-for-retail-channel.md) en maakt deel uit van de Commerce SDK. Het voorbeeld bevindt zich in de map **src\\FiscalIntegration\\Efr** van de opslagplaats [Dynamics 365 Commerce Solutions](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Het [voorbeeld](fiscal-integration-for-retail-channel.md#fiscal-registration-process-and-fiscal-integration-samples-for-fiscal-devices-and-services) bestaat uit een fiscale documentprovider, die een extensie van CRT is, en een fiscale connector, die een extensie is van Commerce Hardware Station. Voor meer informatie over het gebruik van de Commerce SDK, gaat u naar [Commerce SDK-voorbeelden en referentiepakketten van GitHub downloaden en NuGet](../dev-itpro/retail-sdk/retail-sdk-overview.md) en [Een build-pipeline instellen voor de onafhankelijke verpakkings-SDK](../dev-itpro/build-pipeline.md).

> [!NOTE]
> Het voorbeeld van de belastingregistratieservice voor Duitsland is beschikbaar in de Commerce SDK vanaf Commerce versie 10.0.29. In Commercie versie 10.0.28 of eerder moet u de vorige versie van de Retail SDK gebruiken op een virtuele machine voor developers in LCS. Zie [Implementatierichtlijnen voor het voorbeeld van fiscale integratie voor Duitsland (verouderd)](emea-deu-fi-sample-sdk.md) voor meer informatie.

### <a name="crt-extension-design"></a>Ontwerp van CRT-extensies

De extensie die een fiscale documentprovider is, heeft tot doel om servicespecifieke documenten te genereren en responsen van de fiscale registratieservice af te handelen.

#### <a name="request-handler"></a>Aanvraaghandler

Er is één aanvraaghandler voor de documentprovider, **DocumentProviderEFRFiscalDEU**. Deze handler wordt gebruikt om fiscale documenten voor de fiscale registratieservice te genereren. De handler wordt overgenomen van de interface **INamedRequestHandler**. De methode **HandlerName** is verantwoordelijk voor het retourneren van de naam van de handler. De handlernaam moet overeenkomen met de naam van de connector-documentprovider die is opgegeven in Commerce Headquarters.

De connector ondersteunt de volgende aanvragen:

- **GetFiscalDocumentDocumentProviderRequest**: deze aanvraag bevat informatie over welk document moet worden gegenereerd. Het retourneert een servicespecifieke document dat in de fiscale registratieservice moet worden geregistreerd.
- **GetFiscalTransactionExtendedDataDocumentProviderRequest**: deze aanvraag retourneert de respons samen met uitgebreide gegevens.

#### <a name="configuration"></a>Configuratie

Het configuratiebestand voor de fiscale documentprovider bevindt zich in **src\\FiscalIntegration\\Efr\\Configurations\\DocumentProviders\\DocumentProviderFiscalEFRSampleGermany.xml** in de opslagplaats [Dynamics 365 Commerce-oplossingen](https://github.com/microsoft/Dynamics365Commerce.Solutions/). Het doel van het bestand is het inschakelen van instellingen van de fiscale documentprovider die moeten worden geconfigureerd vanuit Commerce Headquarters. De bestandsindeling is afgestemd op de vereisten voor de configuratie van fiscale integratie.

### <a name="hardware-station-extension-design"></a>Ontwerp van extensies voor hardwarestation

De extensie die een fiscale connector is, heeft tot doel om te communiceren met de fiscale registratieservice.

De extensie voor hardwarestations is **HardwareStation.Extension.EFRSample**. Het gebruikt het HTTP-protocol om documenten die de CRT-extensie genereert in te dienen bij de fiscale registratieservice. Het verwerkt ook de responsen die van de fiscale registratieservice worden ontvangen.

#### <a name="request-handler"></a>Aanvraaghandler

De aanvraaghandler **EFRHandler** is het invoerpunt voor het afhandelen van aanvragen bij de fiscale registratieservice. Deze handler wordt overgenomen van de interface **INamedRequestHandler**. De methode **HandlerName** is verantwoordelijk voor het retourneren van de naam van de handler. De handlernaam moet overeenkomen met de naam van de fiscale connector die is opgegeven in Commerce Headquarters.

De connector ondersteunt de volgende aanvragen:

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
