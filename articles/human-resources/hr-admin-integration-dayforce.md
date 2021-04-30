---
title: Integratie met Dayforce configureren
description: De integratie tussen Microsoft Dynamics 365 Human Resources en Ceridian Dayforce is afhankelijk van verschillende configuratiestappen, die in dit artikel worden beschreven. Voordat u een betaling kunt verwerken, moet u de integratie configureren in zowel Human Resources als Dayforce.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PersonnelIntegrationConfiguration
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1647b7fbf84a78051e745e918954df32a2e7e1dd
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889999"
---
# <a name="configure-integration-with-dayforce"></a>Integratie met Dayforce configureren

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

De integratie tussen Microsoft Dynamics 365 Human Resources en Ceridian Dayforce is afhankelijk van verschillende configuratiestappen, die in dit artikel worden beschreven. Voordat u een betaling kunt verwerken, moet u de integratie configureren in zowel Human Resources als Dayforce.

Als u een service zoals Dayforce gebruikt voor het uitvoeren van betalingen, moet u de integratie inschakelen in Human Resources. De integratie vereist specifieke gegevens vanuit Human Resources. Daarom moet u controleren of gegevens die zijn toegewezen aan Dayforce, zodanig in Human Resources zijn geconfigureerd dat de integratie wordt ondersteund. De integratie maakt gebruik van de volgende brede categorieën gegevens:

- HRM-gegevens
- Compensatiegegevens
- Salarisgegevens, zoals betalingscycli, salarisperioden en inkomstencodes
- Medewerkergegevens

In dit artikel worden de stappen beschreven die u moet volgen om de integratie in te schakelen. Ook wordt uitgelegd welke typen gegevens en welke configuratiedetails vereist zijn voor de integratie.

## <a name="enable-the-integration"></a>De integratie inschakelen

In Human Resources moet u de integratie inschakelen en de configuratiegegevens invoeren om verbinding te maken met Dayforce. Als u wilt dat de grootboektransactie die wordt geproduceerd wordt geïmporteerd in Microsoft Dynamics 365 Finance, moet u ook een Microsoft Azure-opslagaccount instellen en de verbindingstekenreeks voor Azure Storage invoeren in Finance.

Voer de volgende stappen uit om de integratie in Human Resources in te schakelen.

1. Ga naar de pagina **Systeembeheer** en selecteer **Configuratie van integratie**.
2. Voer het beveiligde FTP-eindpunt (File Transfer Protocol) en het pad naar de beveiligde FTP-map in.
3. Voer de gebruikersnaam en het wachtwoord in van de gebruiker die toegang krijgt tot het beveiligde FTP-eindpunt en het mappad.
4. Test de verbinding, zoals vereist, en stel de optie **Integratie van salarisadministratie inschakelen** in op **Ja**.

Wanneer de integratie is ingeschakeld, worden het pakket voor gegevensexport en de bestanden gemaakt en wordt de frequentie ingesteld. U kunt deze frequentie naar behoefte wijzigen.

Zie de volgende Azure-artikelen voor meer informatie over Azure Storage-accounts en Azure Storage-verbindingstekenreeksen:

- [Informatie over Azure-opslagaccounts](/azure/storage/common/storage-create-storage-account?toc=%2fazure%2fstorage%2ffiles%2ftoc.json)
- [Verbindingstekenreeks voor Azure Storage configureren](/azure/storage/common/storage-configure-connection-string)

### <a name="technical-details-when-payroll-integration-is-enabled"></a>Technische details wanneer integratie van salarisadministratie is ingeschakeld

Het inschakelen van de integratie van de salarisadministratie heeft twee belangrijke effecten:

- Er wordt een gegevensexportproject met de naam Export van integratie van salarisadministratie gemaakt. Dit project bevat de entiteiten en velden die nodig zijn voor de integratie van de salarisadministratie. Als u het project wilt onderzoeken, gaat u naar **Systeembeheer**, selecteert u de tegel **Gegevensbeheer** en opent u het gegevensproject in de lijst met projecten.
- Met deze batchtaak wordt het gegevensexportproject uitgevoerd, wordt het resulterende gegevenspakket gecodeerd en wordt het gegevenspakketbestand overgebracht naar het SFTP-eindpunt dat is geconfigureerd in het scherm **Configuratie van integratie**.

> [!NOTE]
> Het gegevenspakket dat naar het SFTP-eind punt wordt overgebracht, is gecodeerd met een sleutel die uniek is voor het pakket. De sleutel bevindt zich in een Azure-sleutelkluis die alleen toegankelijk is via Ceridian. Het is niet mogelijk om de inhoud van het gegevenspakket te decoderen en te onderzoeken. Als u de inhoud van het gegevenspakket wilt controleren, moet u het gegevensproject Export van integratie van salarisadministratie handmatig exporteren, downloaden en vervolgens openen. Bij een handmatige export wordt er geen codering toegepast of wordt het pakket niet overgedragen.
> Wanneer de integratiebestanden bijvoorbeeld worden verzonden vanuit een UAT- of sandboxomgeving in Dynamics 365 Human Resources naar een Ceridian Dayforce Test-omgeving, kunt u de volgende Key Vault-URL gebruiken: https://payrollintegrationprod.vault.azure.net.

## <a name="configure-your-data"></a>Uw gegevens configureren 

Om salarissen te kunnen verwerken, moet u resourcegegevens configureren in Human Resources. U moet gegevens over de organisatie, zoals taken en functies, instellen samen met informatie over vergoedingen en compensatie. Deze informatie biedt de informatie over dienstverband, salaris en inhoudingen die vereist is om het salaris van werknemers te genereren.

### <a name="human-resource-data"></a>HRM-gegevens

#### <a name="benefits"></a>Vergoedingen 

Human resources biedt hulpmiddelen voor het instellen en onderhouden van de vergoedingen, inhoudingen en compensatieplannen van medewerkers die een organisatie zijn medewerkers biedt.

Wanneer u vergoedingen maakt, moet u rekening houden met de volgende gegevens en configuraties die worden gebruikt in Dayforce.

##### <a name="benefit-plans"></a>Vergoedingsplannen

- Plan (vereist)
- Type (vereist)
- Gevolgen voor salaris (vereist)
- Achterstallige betalingen herstellen
- Inhoudingsmethode
- Inhoudingsprioriteit
- Limietperiode
- Bedrag beperken

##### <a name="benefits"></a>Vergoedingen

- Plan (vereist)
- Type (vereist)
- Optie (vereist)
- Vergoeding-id (vereist)
- Frequentie
- Basis
- Bedrag of tarief
- Inkomstencode

##### <a name="supported-frequencies"></a>Ondersteunde frequenties 

- Wekelijks
- Tweewekelijks
- Halfmaandelijks
- Maandelijks

##### <a name="supported-bases"></a>Ondersteund bases 

- Vast bedrag
- Percentage van inkomsten
- Productieve uren

Dayforce maakt de volgende inhoudingen, op basis van de salarisgevolgen die zijn gedefinieerd voor het vergoedingsplan.

| Selectie in Human Resources        | Resultaat in Dayforce                            |
|----------------------------|-----------------------------------------------|
| Geen                       | Er wordt geen inhouding gemaakt.                      |
| Alleen inhouding             | Er wordt een inhouding voor de werknemer gemaakt.             |
| Alleen bijdrage          | Er wordt een inhouding voor de werkgever gemaakt.             |
| Inhouding en bijdrage | Er worden inhoudingen voor werknemer en werkgever gemaakt. |

Zie de volgende artikelen voor meer informatie over het definiëren en beheren van een vergoedingsprogramma:

- [Een vergoedingenprogramma voor werknemers maken](/dynamics365/unified-operations/fin-and-ops/hr/tasks/deliver-employee-benefits-program)
- [Een nieuwe vergoeding maken](/dynamics365/unified-operations/fin-and-ops/hr/tasks/create-new-benefit)
- [Regels en beleid van de vergoedingsgeschiktheid definiëren](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-benefit-eligibility-rules-policies)
- [Vergoedingen inschrijven en verwijderen van medewerkers](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-remove-benefits-workers)

#### <a name="compensation"></a>Compensatie 

Compensatiebeheer wordt gebruikt om de betaling van basisloon en beloningen te beheren. Het vaste basissalaris en verdiensteverhogingen van een werknemer worden via vaste compensatieplannen beheerd. De betaling van prestatiebeloningen, zoals bonusbetalingen, beloningen voor prestaties, aandelenopties, en subsidies en ook eenmalige beloningen, worden gecontroleerd door middel van plannen voor variabele compensatie.

Dayforce gebruikt compensatie-informatie voor het berekenen van het uur- of jaartarief van een werknemer. Er zijn vastecompensatieplannen en conversies van het loontarief vereist. Werknemers moeten worden gekoppeld aan een vastecompensatieplan.

Zie de volgende artikelen voor meer informatie over compensatieplannen:

- [Plannen voor vaste compensatie maken](/dynamics365/unified-operations/talent/create-fixed-compensation-plans)
- [Plannen voor variabele compensatie maken](/dynamics365/unified-operations/talent/create-variable-compensation-plans)
- [Salaris-/compensatiestructuur en -plannen ontwikkelen](/dynamics365/unified-operations/fin-and-ops/hr/tasks/develop-salary-compensation-structure-plan)
- [Compensatie verwerken](/dynamics365/unified-operations/talent/process-compensation)
- [Compensatieproces definiëren en resultaten berekenen](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-compensation-process-calculate-results)
- [Een werknemer inschrijven voor een vaste honoreringsregeling](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-fixed-compensation-plan)
- [Een werknemer inschrijven voor een variabele honoreringsregeling](/dynamics365/unified-operations/fin-and-ops/hr/tasks/enroll-employee-variable-compensation-plan)

#### <a name="jobs"></a>Taken 

Een functie is een verzameling taken en verantwoordelijkheden die vereist zijn voor iedere persoon die een functie uitvoert. Zie de volgende artikelen voor meer informatie:

- [De onderdelen van een taak instellen](/dynamics365/unified-operations/talent/create-job)
- [Nieuwe taken definiëren](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-jobs)

##### <a name="positions"></a>Posities

Een positie is een afzonderlijk exemplaar van een taak. De positie 'Verkoopmanager (Oost)' is bijvoorbeeld een van de posities die zijn gekoppeld aan de functie 'Verkoopmanager'. Een positie bestaat op een afdeling. Aan elke positie kan slechts één medewerker worden gekoppeld.

Let op de volgende gegevens en configuratie bij het instellen van posities:

- Positie (vereist)
- Beschrijving (vereist)
- Functie (vereist)
- Afdeling (vereist)
- Positietype (vereist)
- Voltijdse equivalent
- Jaarlijkse normale uren (vereist)
- Betaald door rechtspersoon (vereist)
- Betalingscyclus (vereist)
- Standaard financiële dimensie: kostenplaats (vereist)
- Medewerkertoewijzing: medewerker, toewijzing begin, einde toewijzing, redencode

Als meerdere posities op dezelfde afdeling aan dezelfde functie zijn gekoppeld, worden deze geconsolideerd in een enkele positie in Dayforce.

Zie de volgende artikelen voor meer informatie:

- [Uw werknemers organiseren met afdelingen, taken en posities](/dynamics365/unified-operations/talent/departments-jobs-positions#positions)
- [Posities instellen](/dynamics365/unified-operations/fin-and-ops/hr/tasks/set-up-positions)

#### <a name="departments"></a>Afdelingen

Een afdeling is een operationele eenheid die een categorie of functioneel onderdeel van een organisatie voorstelt. Een afdeling is verantwoordelijk voor een specifiek gebied van de organisatie, zoals verkoop, boekhouding of HR. U kunt afdelingen gebruiken om te rapporteren over functiegebieden. Afdelingen zijn mogelijk verantwoordelijk voor winst en verlies.

Zie de volgende artikelen voor meer informatie:

- [Een afdeling maken en koppelen aan de afdelingshiërarchie](/dynamics365/unified-operations/talent/create-department-add-department-hierarchy)
- [Nieuwe afdelingen definiëren](/dynamics365/unified-operations/fin-and-ops/hr/tasks/define-new-departments)

#### <a name="pay-cycles-and-pay-periods"></a>Betalingscycli en salarisperioden

Een betalingscyclus bepaalt hoe vaak salarissen worden berekend en op welke specifieke dagen medewerkers worden uitbetaald. Zo kan bijvooorbeeld een betalingscyclus maandelijks zijn en kunnen werknemers worden uitbetaald op de laatste dag van de maand. Een betalingscyclus kan ook wekelijks en werknemers kunnen worden uitbetaald op de dinsdag na het einde van de salarisperiode. Betalingscycli zijn toegewezen aan posities om te bepalen wanneer medewerkers in deze posities worden uitbetaald.

Nadat u betalingscycli hebt gemaakt, kunt u salarisperioden voor elke cyclus genereren. Elke salarisperiode bevat een standaard betalingsdatum die is gebaseerd op gegevens die u verstrekt. U kunt echter de standaard betalingsdatum in een salarisperiode wijzigen om te voorzien in uitzonderingen, bijvoorbeeld wanneer de betalingsdatum op een feestdag valt.

De volgende informatie wordt gebruikt in Dayforce:

- Betalingscyclus (vereist)
- Frequentie van betalingscyclus (vereist)
- Begindatum van periode (eerste salarisperiode vereist)
- Standaardbetalingsdatum (eerste salarisperiode vereist)

Deze informatie is geïntegreerd met Dayforce als betalingsgroepen en worden gescheiden per land of regio voor elke betalingscyclus. Vóór integratie moet ten minste één salarisperiode worden gegenereerd. Dayforce genereert van betalingsgroepkalenders en betalingsdatums, op basis van de begindatum van de eerste salarisperiode en de standaardbetalingsdatum die is ingesteld in Human Resources.

#### <a name="earning-codes"></a>Inkomstencodes

Inkomstencodes bieden een unieke identificatie van elk type inkomsten dat medewerkers ontvangen. De codes hebben verschillende parameters die betrekking hebben op inkomsten, zoals boekhoudkundige regels, belastingwetgeving, rapportagevereisten en mogelijkheden voor gebruik van brutowaarden.

De volgende informatie wordt gebruikt in Dayforce:

- Inkomstencode (vereist)
- Omschrijving
- Maateenheid
- Productief

### <a name="worker-data"></a>Medewerkergegevens

Records voor de verschillende soorten medewerkers die u hebt zijn belangrijk voor uw HRM- en salarisadministratiesystemen. De gegevens die u invoert, kunnen worden gebruikt om medewerkers en persoonlijke gegevens bij te houden.

U kunt de volgende informatie bijhouden voor medewerkers:

- **Basis** – Basisinformatie over een medewerker bijhouden, zoals contactgegevens, demografische gegevens, identificatiegegevens, informatie over de familie, status van militaire dienst, expat-informatie en contactpersonen voor noodgevallen.
- **Dienstverband** – Informatie bijhouden over werkgelegenheid van een medewerker, zoals een aansluiting met een bedrijf of organisatie, functie, start- en einddatums, arbeidsgeschiktheid, arbeidsvoorwaarden, pensioen, verlof en relocatie-informatie.
- **Verlof en verzuim** – Informatie bijhouden over de afwezigheid van een medewerker, zoals werkkalenders, verzuimtransacties en verzuiminstellingen.
- **Vergoedingen en salarissen** – Informatie bijhouden over compensatieplannen en salarisgegevens van een medewerker zoals inschrijving op plan, onderscheidingen, commissie, fiscale informatie, pensioen en salarisinhoudingen.

Wanneer u informatie over een werknemer invoert, moet u rekening houden met de volgende gegevens en configuraties die worden gebruikt in Dayforce.

#### <a name="general-information"></a>Algemene informatie

- Personeelsnummer (vereist)
- Voornaam (vereist)
- Achternaam (vereist)
- Tweede naam
- Anciënniteitsdatum
- Bekend als

#### <a name="personal-information"></a>Persoonlijke informatie

- Burgerlijke staat (vereist)
- Geboortedatum (vereist)
- Geslacht (vereist)
- Persoon met handicap
- Land/regio nationaliteit (alleen voor Mexico)

#### <a name="address-information"></a>Adresgegevens

- Primair (vereist)
- Land/regio (vereist)
- Postcode (vereist)
- Huisnummer (vereist) (alleen voor Mexico)
- Gebouwtoevoeging (alleen voor Mexico)
- Plaats (vereist)
- Staat (vereist)
- District (vereist)

#### <a name="contact-information"></a>Gegevens contactpersoon 

- Primair (vereist)
- Contactnummer (vereist)
- Toestel

#### <a name="payroll-information-and-earning-codes"></a>Salarisinformatie en inkomstencodes

Aan werknemers kunnen bepaalde inkomsten met een bepaalde betalingsfrequentie worden toegewezen en zij kunnen een geprefereerde betalingsmethode hebben. De volgende velden worden gebruikt in Dayforce om te garanderen dat deze voorkeuren en instellingen worden gebruikt.

##### <a name="earning-codes"></a>Inkomstencodes

- Positie (vereist)
- Inkomstencode (vereist)
- Frequentie (vereist)
- Bedrag (vereist)

##### <a name="payroll-information"></a>Salarisinformatie

- Betalingsmethode
- Economische regio (vereist)
- Id personeelsvergoedingen
- Nationaal id-nummer (vereist)
- Nummer militaire dienst
- Ploeg-id (vereist)
- Btw-nummer (vereist)
- Vakbond-id (vereist)
- Werkdag-id (vereist)
- Nummer werkvergunning

> [!NOTE]
> Voor de betalingsmethode ondersteunt Mexico **Contant geld**, **Cheque** (de fysieke cheque van het bedrijf) en **Elektronische betaling**. Als geen betalingsmethode is opgegeven, wordt standaard **Cheque** gebruikt.

#### <a name="employment-details"></a>Details dienstverband

Historische gegevens over het dienstverband worden gebruikt als belangrijkste informatie voor het opvragen van de statussen voor aanstellen, ontslaan en opnieuw aanstellen van een werknemer in Dayforce. Dayforce ondersteunt slechts één actieve dienstverbandrecord tegelijk.

- Begindatum dienstverband (vereist)
- Einddatum dienstverband
- Begindatum
- Aangepaste begindatum
- Ontslagdatum (vereist bij ontslag)
- Ontslagreden (vereist bij ontslag)

De belangrijkste datums van een werknemer worden afgeleid met behulp van de volgende gegevens.

| Human resources                | Dayforce                                                                                             |
|-----------------------|------------------------------------------------------------------------------------------------------|
| Meest recente huurdatum | Begindatum van dienstverband van historierecord van huidig niet-beëindigd dienstverband                                 |
| Ontslagdatum      | Ontslagdatum van historierecord van huidig niet-beëindigd dienstverband                                 |
| Begindatum            | Aangepaste begindatum, begindatum of begindatum dienstverband van historierecord van huidig niet-beëindigd dienstverband |
| Oorspronkelijke datum indiensttreding    | Begindatum dienstverband van vroegste historierecord van dienstverband                                               |

#### <a name="compensation"></a>Compensatie

Een vastecompensatieplan moet worden gekoppeld aan de primaire functie van elke werknemer tijdens de hele duur van het dienstverband. Deze periode begint op de datum waarop de werknemer in dienst is genomen (of de begindatum van het dienstverband) en gaat door totdat aan het ontslag.

- Ingangsdatum (vereist)
- Vervaldatum
- Loontarief (vereist)
- Conversies van loontarief (vereist)
- Jaarlijks equivalent (vereist)
- Uurequivalent (vereist)

Als een werknemer met uurtarief meerdere posities heeft, wordt de vaste compensatie van de primaire positie geïmporteerd in Dayforce als het basistarief/-salaris op werknemerniveau. Voor niet-primaire posities, wordt het uurtarief opgeslagen bij de overeenkomende positie in Dayforce.

Als een medewerker met een salaris meerdere posities heeft, worden het cumulatieve uurtarief en het jaarsalaris voor alle actieve posities afgeleid en gebruikt als de basistarief/-salaris op werknemerniveau.

#### <a name="identification-numbers"></a>Identificatienummers

##### <a name="social-security-identifier"></a>Sociaal-fiscaal nummer 

Elke werknemer moet één primaire id hebben. Deze id moet van het identificatietype **Sofinummer** zijn. In Dayforce, wordt dit automatisch afgeleid als het sociaal-fiscaal nummer van de werknemer dat is vereist voor aanstelling.

- Primair (vereist)
- Identificatietype = 'Sofinummer'
- Uitgiftedatum
- Vervaldatum

Werknemers kunnen meerdere identificatienummers van het identificatietype **Sofinummer** opgeven. Alleen de record die is gemarkeerd als **Primair** wordt echter opgenomen in Dayforce, ongeacht of het nummer actief of verlopen is.

#### <a name="bank-accounts-and-disbursements"></a>Bankrekeningen en voorschotten

Er moet geldige bankrekeninginformatie worden ingevoerd voor elke werknemer die wil worden uitbetaald via bankrekeningoverboekingen.

| Human resources                         | Dayforce                                                                                                    |
|--------------------------------|-------------------------------------------------------------------------------------------------------------|
| Bankrekeningnummer (vereist) |                                                                                                             |
| SWIFT-code (vereist)          | Veld **Bank-id** dat wordt gebruikt bij het verwerken van salarissen in Mexico.                                                             |
| Vestigingsnummer (vereist)       |                                                                                                             |
| Bankrekeningtype (vereist)   | Veld **Rekeningtype** dat wordt gebruikt bij het verwerken van salarissen in Mexico. Ondersteunde waarden zijn **Rekening-courant** en **Salaris**. |

> [!NOTE]
> Werknemers die ervoor kiezen om te worden uitbetaald via bankrekeningoverboekingen moeten een koppeling opgeven naar een restantrekening die zich onder een rechtspersoon bevindt met het primaire adres in Mexico en die is gekoppeld aan een geldige bankrekening van een Mexicaanse bank. Alle andere niet-restantrekeningen worden genegeerd.

#### <a name="address-information"></a>Adresgegevens

Elke werknemer moet één primaire locatie hebben. In Dayforce wordt deze locatie gebruikt om de primaire woonplaats van de werknemer te bepalen voor belastingdoeleinden.

- Primair (vereist)
- Land/regio (vereist)
- Postcode (vereist)
- Straat (vereist)
- Huisnummer (vereist)
- Gebouwtoevoeging
- Plaats (vereist)
- Staat (vereist)
- District (vereist)

## <a name="configure-your-data-to-generate-payroll-in-united-states-and-canada"></a>Uw gegevens configureren voor het genereren van salarissen in de Verenigde Staten en Canada

Als u salarissen genereert voor werknemers in de Verenigde Staten en Canada, moeten de volgende elementen worden geconfigureerd:

- Afdelingen zijn vereist voor posities.
- Kostenplaatsen moeten worden ingesteld als financiële dimensies en moeten het eerste element in de standaardtekenreeks voor de financiële dimensie vormen.

> [!NOTE] 
> U kunt Human Resources zo configureren dat wordt vereist dat met posities een afdeling wordt opgegeven. Hiertoe gaat u naar **Gedeelde Human Resources-posities > Posities > Afdelingen voor posities vereisen**. Het wordt aanbevolen deze instelling af te dwingen voor de integratie.

### <a name="job-types"></a>Functietypen

Functietypen worden gebruikt om vergelijkbare functies in categorieën te groeperen. Functietypen zijn vereist voor het verwerken van salarissen in de Verenigde Staten en Canada. Voorbeelden van functietypen zijn onder anderen fulltime en parttime of salaris en uurtarief. Functietypen worden toegewezen aan Dayforce als salaristypen die aangeven of een werknemer per uur wordt betaald of een salaris ontvangt.

De volgende functietypen en omschrijvingen zijn vereist.

| Functietype   | Omschrijving |
|------------|-------------|
| Per uur     | Per uur      |
| Bezoldigd   | Bezoldigd    |

### <a name="position-types"></a>Positietypen 

U gebruikt positietypen om te beschrijven of de positie fulltime, parttime of iets anders is. Positietypen worden toegewezen aan Dayforce als betalingsklassen die aangeven of een werknemer een fulltime of parttime dienstverband heeft.

De volgende positietypen en omschrijvingen zijn vereist.

| Positietype   | Omschrijving        |
|-----------------|--------------------|
| Voltijd       | Voltijdse werknemer |
| Deeltijd       | Werknemer in deeltijd |

### <a name="reason-codes"></a>Redencodes

Redencodes bieden informatie over de status van een werknemer. Redencodes worden toegewezen aan Dayforce als statusredenen die de reden voor wijzigingen in de positie of de status van het dienstverband van een werknemer aangeven.

De volgende redencodes en omschrijvingen zijn vereist.

| Redencode    | Omschrijving      | Toepasselijke scenario's |
|----------------|------------------|----------------------|
| RESIGNATION    | Ontslag      | Medewerker ontslaan     |
| TERMINATION    | Beëindiging      | Medewerker ontslaan     |
| RETIREMENT     | Pensionering       | Medewerker ontslaan     |
| OTHER          | Andere redenen    | Medewerker ontslaan     |
| DEATH          | Overlijden            | Medewerker ontslaan     |
| LEAVEOFABSENCE | Verlof of verzuim | Medewerker ontslaan     |
| CONTRACTEND    | Einde van contract  | Medewerker ontslaan     |
| SALARYCHANGE   | Salariswijziging | Compensatie         |

### <a name="marital-status"></a>Burgerlijke staat

De waarden voor de burgerlijke staat worden toegewezen aan Dayforce en, waar nodig, vertaald naar de geaccepteerde waarden bij integratie.

In de volgende tabel wordt aangegeven hoe de waarden voor de burgerlijke staat worden toegewezen aan Dayforce.

| Human resources                 | Dayforce             |
|------------------------|----------------------|
| Gehuwd                | Gehuwd              |
| Eén                 | Eén               |
| Weduwe/weduwnaar                | Weduwe/weduwnaar              |
| Gescheiden               | Gescheiden             |
| Geregistreerd partnerschap | Binnenlands partnerschap |
| None                   | None                 |
| Samenwonend             | Samenwonend           |

### <a name="gender"></a>Geslacht

Geslachtsaanduidingen worden toegewezen aan Dayforce en, waar nodig, vertaald naar de geaccepteerde waarden bij integratie.

In de volgende tabel wordt aangegeven hoe geslachtsaanduidingen worden toegewezen aan Dayforce.

| Human resources       | Dayforce        |
|--------------|-----------------|
| Mannelijk         | Mannelijk            |
| Vrouwelijk       | Vrouwelijk          |
| Niet-specifiek | *Niet ondersteund* |

### <a name="earning-codes"></a>Inkomstencodes

Inkomstencodes bieden een unieke identificatie van elk type inkomsten dat medewerkers ontvangen. De codes bevatten verschillende parameters die betrekking hebben op inkomsten, zoals boekhoudkundige regels, belastingwetgeving, rapportagevereisten en mogelijkheden voor gebruik van brutowaarden. Als een niet-ondersteunde frequentie wordt gebruikt, wordt standaard de frequentie **Elke betaling** gebruikt voor de berekening.

#### <a name="supported-frequencies"></a>Ondersteunde frequenties

- Alles
- EVERYPAY
- EACHPAYPERIOD
- EVRYOTHRPAYODD
- EVRYOTHRPAYEVN
- 1OFMTH
- LASTOFMTH
- 2OFMTH
- 3OFMTH
- 4OFMTH
- 5OFMTH
- 1N2OFMTH
- 3N4OFMTH
- 1N3OFMTH
- 1N4OFMTH
- 2N3OFMTH
- 2N4OFMTH
- 1N2N3OFMTH
- 1N2N4OFMTH
- 1N3N4OFMTH
- 2N3N4OFMTH
- 1N2N3N4OFMTH - 1N2N3N4OFMTH
- 2N3N4N5OFMth - 2N3N4N5OFMth
- 1OFQTR - 1OFQTR
- LASTOFQTR – LASTOFQTR
- LASTMTHOFQTR – LASTMTHOFQTR
- 1OFYEAR - 1OFYEAR
- LASTOFYEAR – LASTOFYEAR
- NOVNDECOFYEAR - NOVNDECOFYEAR

### <a name="addresses"></a>Adressen

De identificatie van specifieke codes voor land of regio, staat en district (gemeente) vereist specifieke indelingen die door Dayforce en providers in het land of in de regio kunnen worden herkend. Hoewel de indeling voor plaatsen flexibel is, moet elke plaats worden gekoppeld aan een staat.

| Human resources          | Dayforce              |
|-----------------|-----------------------|
| Land/regio  | Landcode          |
| Postcode | Postcode           |
| Provincie           | Staatcode            |
| Plaats            | Plaats                  |
| District          | District (gemeente) |
| Adres          | Adresregel 1        |

### <a name="tax-regions"></a>Belastingregio's

Belastingregio's worden gebruikt om de juiste belasting te bepalen die moet worden gebruikt bij het genereren van salarissen. Belastingregio's worden aan Dayforce toegewezen als locatieadressen. De standaardbelastingregio moet aan de actieve positie van de werknemer worden gekoppeld. 

- Belastingregio (vereist)
- Land/regio (vereist)
- Staat (vereist)
- District 
- Plaats (vereist)

## <a name="configure-your-data-to-generate-payroll-in-mexico"></a>Uw gegevens configureren voor het genereren van salarissen in Mexico

Als u salarissen genereert voor werknemers in Mexico, moeten de volgende elementen worden geconfigureerd:

- Afdelingen zijn vereist voor posities.
- Kostenplaatsen moeten worden ingesteld als financiële dimensies en moeten het eerste element in de standaardtekenreeks voor de financiële dimensie vormen.

### <a name="job-types"></a>Taaktypen

Functietypen worden gebruikt om vergelijkbare functies in categorieën te groeperen. Functietypen zijn vereist voor het verwerken van salarissen in Mexico. Voorbeelden van functietypen zijn onder anderen fulltime en parttime of salaris en uurtarief. Functietypen worden toegewezen aan Dayforce als salaristypen die aangeven of een werknemer per uur wordt betaald of een salaris ontvangt.

De volgende functietypen en omschrijvingen zijn vereist.

| Functietype   | Omschrijving |
|------------|-------------|
| Per uur     | MX Per uur   |
| Bezoldigd   | MX Bezoldigd |

### <a name="position-types"></a>Positietypen 

U gebruikt positietypen om te beschrijven of de positie fulltime, parttime of iets anders is. Positietypen worden toegewezen aan Dayforce als betalingsklassen die aangeven of een werknemer een fulltime of parttime dienstverband heeft.

De volgende positietypen en omschrijvingen zijn vereist.

| Positietype   | Omschrijving        |
|-----------------|--------------------|
| Voltijd       | Voltijdse werknemer |
| Deeltijd       | Werknemer in deeltijd |

### <a name="reason-codes"></a>Redencodes

Redencodes bieden informatie over de status van een werknemer. Redencodes worden toegewezen aan Dayforce als statusredenen die de reden voor wijzigingen in de positie of de status van het dienstverband van een werknemer aangeven.

De volgende redencodes en omschrijvingen zijn vereist.

| Redencode            | Omschrijving                    | Toepasselijke scenario's |
|------------------------|--------------------------------|----------------------|
| DEPARTUREBEFOREPAYMENT | Vertrek voor eerste salaris | Medewerker ontslaan     |
| RESIGNATION            | Ontslag                    | Medewerker ontslaan     |
| PENSION                | Pensioen                        | Medewerker ontslaan     |
| TERMINATION            | Beëindiging                    | Medewerker ontslaan     |
| RETIREMENT             | Pensionering                     | Medewerker ontslaan     |
| ABSENTEE               | Verzuim                       | Medewerker ontslaan     |
| OTHER                  | Andere redenen                  | Medewerker ontslaan     |
| CLOSURE                | Bedrijfssluiting               | Medewerker ontslaan     |
| DEATH                  | Overlijden                          | Medewerker ontslaan     |
| LEAVEOFABSENCE         | Verlof of verzuim               | Medewerker ontslaan     |
| CONTRACTEND            | Einde van contract                | Medewerker ontslaan     |
| SALARYCHANGE           | Salariswijziging               | Compensatie         |

### <a name="terms-of-employment"></a>Arbeidsvoorwaarden

Arbeidsvoorwaarden worden gebruikt om categorieën met arbeidsvoorwaarden te maken. De voorwaarden worden toegewezen aan Dayforce als indicatorwaarden voor het dienstverband.

De volgende arbeidsvoorwaarden en omschrijvingen zijn vereist.

| Arbeidsvoorwaarden   | Omschrijving |
|-----------------------|-------------|
| Normaal               | Normaal     |
| Direct                | Direct      |
| Stage            | Stage  |
| Permanent             | Permanent   |

### <a name="marital-status"></a>Burgerlijke staat

De waarden voor de burgerlijke staat worden toegewezen aan Dayforce en, waar nodig, vertaald naar de geaccepteerde waarden bij integratie.

In de volgende tabel wordt aangegeven hoe de waarden voor de burgerlijke staat worden toegewezen aan Dayforce.

| Human resources                 | Dayforce                  |
|------------------------|---------------------------|
| Gehuwd                | Gehuwd                   |
| Eén                 | Eén                    |
| Weduwe/weduwnaar                | Weduwe/weduwnaar                   |
| Gescheiden               | Gescheiden                  |
| Geregistreerd partnerschap | Binnenlands partnerschap      |
| None                   | *Niet ondersteund door Mexico* |
| Samenwonend             | *Niet ondersteund door Mexico* |

### <a name="gender"></a>Geslacht

Geslachtsaanduidingen worden toegewezen aan Dayforce en, waar nodig, vertaald naar de geaccepteerde waarden bij integratie.

In de volgende tabel wordt aangegeven hoe geslachtsaanduidingen worden toegewezen aan Dayforce.

| Human resources       | Dayforce                  |
|--------------|---------------------------|
| Mannelijk         | Mannelijk                      |
| Vrouwelijk       | Vrouwelijk                    |
| Niet-specifiek | *Niet ondersteund door Mexico* |

### <a name="payment-method"></a>Betalingsmethode

Betalingsmethoden bieden de werknemer en het bedrijf een manier om te beschrijven hoe werknemers worden uitbetaald. Betalingsmethoden worden toegewezen aan Dayforce en, waar nodig, vertaald naar de geaccepteerde waarden bij integratie.

In de volgende tabel wordt aangegeven hoe betalingsmethoden worden toegewezen aan Dayforce.

| Human resources             | Dayforce                  |
|--------------------|---------------------------|
| Contant geld               | Contant geld                      |
| Elektronische betaling | Overboeking                  |
| Controleren              | Cheque                    |
| Bankcheque         | *Niet ondersteund door Mexico* |
| Overig              | *Niet ondersteund door Mexico* |

### <a name="bank-account-type"></a>Bankrekeningtype

Bankrekeningtypen worden gebruikt voor elektronische betalingen aan werknemers. Bankrekeningtypen worden toegewezen aan Dayforce als overdrachtrekeninggegevens. De bankrekeningtypen worden, waar nodig, vertaald naar de geaccepteerde waarden bij integratie.

| Human resources            | Dayforce                  |
|-------------------|---------------------------|
| Betaalrekening  | CheckingAccount           |
| Salarisrekening   | PayrollAccount            |
| Spaarrekening   | *Niet ondersteund door Mexico* |
| BankGirot-rekening | *Niet ondersteund door Mexico* |
| PlusGirot-rekening | *Niet ondersteund door Mexico* |

### <a name="earning-codes"></a>Inkomstencodes

Inkomstencodes bieden een unieke identificatie van elk type inkomsten dat medewerkers ontvangen. De codes bevatten verschillende parameters die betrekking hebben op inkomsten, zoals boekhoudkundige regels, belastingwetgeving, rapportagevereisten en mogelijkheden voor gebruik van brutowaarden. Als een niet-ondersteunde frequentie wordt gebruikt, wordt standaard de frequentie **Elke betaling** gebruikt voor de berekening.

#### <a name="supported-frequencies"></a>Ondersteunde frequenties

- Alles
- EVERYPAY
- EACHPAYPERIOD
- EVRYOTHRPAYODD
- EVRYOTHRPAYEVN
- 1OFMTH
- LASTOFMTH
- 2OFMTH
- 3OFMTH
- 4OFMTH
- 5OFMTH
- 1N2OFMTH
- 3N4OFMTH
- 1N3OFMTH
- 1N4OFMTH
- 2N3OFMTH
- 2N4OFMTH
- 1N2N3OFMTH
- 1N2N4OFMTH
- 1N3N4OFMTH
- 2N3N4OFMTH
- 1N2N3N4OFMTH - 1N2N3N4OFMTH
- 2N3N4N5OFMth - 2N3N4N5OFMth
- 1OFQTR - 1OFQTR
- LASTOFQTR – LASTOFQTR
- LASTMTHOFQTR – LASTMTHOFQTR
- 1OFYEAR - 1OFYEAR
- LASTOFYEAR – LASTOFYEAR
- NOVNDECOFYEAR - NOVNDECOFYEAR

### <a name="addresses"></a>Adressen

De identificatie van specifieke codes voor land of regio, staat en district (gemeente) vereist specifieke indelingen die door Dayforce en providers in het land of in de regio kunnen worden herkend. Hoewel de indeling voor plaatsen flexibel is, moet elke plaats worden gekoppeld aan een staat.

| Human resources              | Dayforce              |
|---------------------|-----------------------|
| Land/regio      | Landcode          |
| Postcode     | Postcode           |
| Provincie               | Staatcode            |
| Plaats                | Plaats                  |
| District              | District (gemeente) |
| Adres              | Adresregel 1        |
| Huisnummer       | Adresregel 2        |
| Gebouwtoevoeging | Adresregel 5        |

### <a name="passport-number"></a>Paspoortnummer

Werknemers kunnen paspoortgegevens opgeven. Deze informatie is van het identificatietype **Paspoort** en wordt in Dayforce geïntegreerd als onderdeel van de Mexico-specifieke informatie van een werknemer.

- Identificatietype = 'Paspoort'
- Uitgiftedatum
- Vervaldatum

Werknemers kunnen meerdere identificatienummers van het identificatietype **Paspoort** opgeven. Echter alleen de huidige actieve paspoortvermelding wordt geïntegreerd in Dayforce. Als alle paspoortvermeldingen zijn verlopen, wordt het paspoort dat als laatste is uitgegeven geïntegreerd in Dayforce.



[!INCLUDE[footer-include](../includes/footer-banner.md)]