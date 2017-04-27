---
title: Afgeschafte functies
description: "Dit onderwerp beschrijft de functies die zijn verwijderd of zijn in gepland voor verwijdering uit Dynamics van 365 for Operations. Het bevat ook functies die in Dynamics AX 7.0-versies zijn beëindigd."
author: sericks007
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Operations, Platform
ms.custom: 21821
ms.assetid: 31019808-4cbf-47d7-b1ba-d791db4281ae
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: e9ba7239b9ff8b9b97c9dabc06fb2c68760d19d4
ms.lasthandoff: 03/31/2017


---

# <a name="deprecated-features"></a>Afgeschafte functies

Dit onderwerp beschrijft de functies die zijn verwijderd of zijn in gepland voor verwijdering uit Dynamics van 365 for Operations. Het bevat ook functies die in Dynamics AX 7.0-versies zijn beëindigd.

<a name="features-that-have-been-deprecated-in-dynamics-365-for-operations-1611-with-platform-update-3"></a>Functies die in Dynamics 365 for Operations 1611 met platformupdate 3 zijn verwijderd
---------------------------------------------------------------------------------------------

### <a name="aeb-payment-formats-for-spain"></a>AEB-betalingsindelingen voor Spanje

In Spanje worden CSB-betalingsindelingen (Consejo Superior Bancario) gebruikt om remisebestanden naar de bank te verzenden voor klant- en leveranciersbetalingen. De inhoud van deze indelingen wordt bepaald door de Asociación Española de Banca (AEB). Dit dekt Cuaderno 19, 32, 58, 34.

|                              |                                                                          |
|------------------------------|--------------------------------------------------------------------------|
| Reden voor afschrijving       | De betalingsindelingen worden niet meer gebruikt.                                  |
| Vervangen door een andere functie? | Ja, ISO20022-indelingen voor kredietoverdracht en automatische overschrijvingen voor Spanje |
| Modules die worden beïnvloed             | Leveranciers, Klanten                                    |

### <a name="bank-payments-transfer-for-lithuania"></a>Overboeking van bankbetalingen voor Litouwen

Bankbetalingsoverboekingen worden gegenereerd en afgedrukt met de exportindeling voor betalingsoverboekingen (LT) voor Litouwen. De Litouwse markt gebruikt vanaf 2005 LITAS, het universele elektronische bankiersysteem.

|                              |                                                            |
|------------------------------|------------------------------------------------------------|
| Reden voor afschrijving       | De betalingsindelingen worden niet meer gebruikt.                    |
| Vervangen door een andere functie? | Ja, ISO20022-indeling voor kredietoverdrachtbetalingen voor Litouwen |
| Modules die worden beïnvloed             | Leveranciers                                               |

### <a name="bbs-direkte-remittering-payment-formats-for-norway"></a>Betalingsindelingen van BBS Direkte voor Remittering voor Noorwegen

Betalingsindelingen voor BBS Direkte Remittering omvatten export van incasso met klantbetalingen (automatische afschrijving) en import van retourbericht.

|                              |                                                                                                                                                                |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | De betalingsindelingen worden niet meer gebruikt.                                                                                                                        |
| Vervangen door een andere functie? | De AvtaleGiro-klantbetalingsindeling voor Noorwegen kan worden gebruikt om berichten voor automatische afschrijving te genereren. Het importeren van het retourbericht wordt geïmplementeerd in toekomstige versies. |
| Modules die worden beïnvloed             | Leveranciers, Klanten                                                                                                                          |

### <a name="chart-of-accounts-tool-for-spain"></a>Rekeningschematool voor Spanje

Deze tool wordt gebruikt wanneer een rekeningschema in Spanje belangrijke wijzigingen vereist. Gebruikers kunnen een nieuw rekeningschema in Microsoft Excel- of tekstindeling importeren, en kunnen ook financiële overzichten importeren.

|                              |                |
|------------------------------|----------------|
| Reden voor afschrijving       | Beperkt gebruik  |
| Vervangen door een andere functie? | Nee             |
| Modules die worden beïnvloed             | Grootboek |

### <a name="dom80-payment-format-for-belgium"></a>Dom80-betalingsindeling voor België

Verouderde Belgische betalingsindeling voor het innen van betalingen (automatische afschrijving).

|                              |                                                        |
|------------------------------|--------------------------------------------------------|
| Reden voor afschrijving       | De betalingsindeling wordt niet meer gebruikt.                  |
| Vervangen door een andere functie? | Ja, ISO 20022-betalingsindeling voor automatische afschrijving voor België |
| Modules die worden beïnvloed             | Klanten                                      |

### <a name="dtaezag-payment-formats-for-switzerland"></a>DTA/EZAG-betalingsindelingen voor Zwitserland

DTA/EZAG-indelingen worden geïntegreerd in het ESR-systeem omdat ze een referentienummer kunnen hebben. Omdat de referentienummers niet verplicht zijn, kunnen alle leveranciersbetalingen worden verwerkt met deze indelingen. Deze indelingen worden gebruikt door bedrijven die een bankrekening op een locatie buiten Postfinance hebben.

|                              |                                                              |
|------------------------------|--------------------------------------------------------------|
| Reden voor afschrijving       | De betalingsindelingen worden niet meer gebruikt.                      |
| Vervangen door een andere functie? | Ja, ISO20022-betalingsindeling voor kredietoverdracht voor Zwitserland |
| Modules die worden beïnvloed             | Leveranciers                                                 |

### <a name="edifact-dirdeb-payment-format-for-austria"></a>EDIFACT-DIRDEB-betalingsindeling voor voor Oostenrijk

EDIFACT-DIRDEB-betalingsindeling voor het innen van betalingen (automatische afschrijving).

|                              |                                                        |
|------------------------------|--------------------------------------------------------|
| Reden voor afschrijving       | De betalingsindeling wordt niet meer gebruikt.                  |
| Vervangen door een andere functie? | Ja, ISO 20022-betalingsindeling voor automatische afschrijving voor Oostenrijk |
| Modules die worden beïnvloed             | Klanten                                      |

### <a name="edivat-for-belgium"></a>EDIVAT voor België

EDIVAT is een verouderde Belgische standaard voor elektronische aangifte via beveiligde post. Microsoft Dynamics AX 2012 behoudt de alleen-lezen oplossing om toegang tot de historische gegevens mogelijk te maken.

|                              |                                      |
|------------------------------|--------------------------------------|
| Reden voor afschrijving       | De functionaliteit wordt niet meer gebruikt. |
| Vervangen door een andere functie? | Nee                                   |
| Modules die worden beïnvloed             | Grootboek                       |

### <a name="egiro-edifact-cremul-payment-import-format-for-norway"></a>eGiro Edifact CREMUL-importindeling voor betalingen in Noorwegen

eGiro is gebaseerd op de internationale UN-standaard EDIFACT CREMUL (Multiple Credit Advice Message) die voor het automatisch boeken van klantbetalingen wordt gebruikt. In Microsoft Dynamics AX wordt eGiro uitgevoerd als importindeling van klantbetalingen.

|                              |                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | De betalingsindeling wordt niet meer gebruikt.                                                     |
| Vervangen door een andere functie? | Nr. De indeling wordt vervangen door ISO 20022-importindelingen voor afschriften in toekomstige versies. |
| Modules die worden beïnvloed             | Klanten                                                                         |

### <a name="external-inventory-for-poland"></a>Externe voorraad voor Polen

Bewijs van goederen die zijn verkregen van een leverancier voor verkopen zonder inkoop. Goederen die in externe voorraad worden verwerkt zijn niet van invloed op de standaardvoorraad, en kunnen worden verkocht en vervolgens automatisch worden ingekocht. Dit proces zorgt voor echte voorraadmutaties.

|                              |                                                 |
|------------------------------|-------------------------------------------------|
| Reden voor afschrijving       | Vervangen door een andere functie                     |
| Vervangen door een andere functie? | Ja, de kernfunctionaliteit van Inkomende consignatie |
| Modules die worden beïnvloed             | Leveranciers, Voorraadbeheer          |

### <a name="financial-reports-generator-for-eastern-europe"></a>Generator Financiële rapporten voor Oost-Europa

Een hulpmiddel om een gegevensverzameling in te stellen voor boekhouding en belastingaangiften, en om gegevens te exporteren naar XLS- en DOC-rapportsjablonen

|                              |                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | Beperkt gebruik                                                                            |
| Vervangen door een andere functie? | Nr. Het hulpmiddel wordt vervangen door Elektronische rapportageconfiguraties in toekomstige versies. |
| Modules die worden beïnvloed             | Grootboek                                                                           |

### <a name="import-of-customer-payment-transactions-for-finland"></a>Importeren van de transacties van klantbetalingen voor Finland

U kunt een importindeling voor Finse betalingen selecteren om de transacties van klantbetalingen te importeren uit een extern bestand dat de bank heeft gegeven.

|                              |                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | De betalingsindeling wordt niet meer gebruikt.                                                     |
| Vervangen door een andere functie? | Nr. De indeling wordt vervangen door ISO 20022-importindelingen voor afschriften in toekomstige versies. |
| Modules die worden beïnvloed             | Klanten                                                                         |

### <a name="import-of-payment-transactions-into-a-general-ledger-journal-for-finland"></a>Importeren van betalingstransacties in een grootboekjournaal voor Finland

Een indeling die specifiek is voor Finland, wordt gebruikt voor het importeren van boekhoudingstransacties in het grootboek.

|                              |                                                                                           |
|------------------------------|-------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | De betalingsindeling wordt niet meer gebruikt.                                                     |
| Vervangen door een andere functie? | Nr. De indeling wordt vervangen door ISO 20022-importindelingen voor afschriften in toekomstige versies. |
| Modules die worden beïnvloed             | Klanten                                                                         |

### <a name="integration-with-isabel-synchronized-cis-for-belgium"></a>Integratie met Isabel gesynchroniseerd (CIS) voor België

Isabel is het framework voor elektronisch bankieren in Europa en een de facto-standaard in België.

|                              |                                                                                                                      |
|------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | Integratie met Isabel-client is beëindigd.                                                                |
| Vervangen door een andere functie? | Nr. De betalingsindelingen die niet meer worden gebruikt, worden vervangen door ISO20022-betalingsindeling voor kredietoverdracht voor België. |
| Modules die worden beïnvloed             | Leveranciers                                                                                                         |

### <a name="modifications-in-the-chart-of-accounts-and-accounting-rules-for-spain"></a>Wijzigingen in het rekeningschema en boekhoudregels voor Spanje

Deze functie wordt gebruikt voor wijzigingen in het rekeningschema en boekhoudregels voor Spanje. Het koppelt rekeningen om het oude rekeningschema te transformeren in het nieuwe rekeningschema, en vergelijkt het vorige boekjaar met het nieuwe boekjaar, zelfs als ze op verschillende rekeningnummers zijn geboekt.

|                              |                |
|------------------------------|----------------|
| Reden voor afschrijving       | Beperkt gebruik  |
| Vervangen door een andere functie? | Nee             |
| Modules die worden beïnvloed             | Grootboek |

### <a name="pagamento-fornittori-vendor-payment-format"></a>De betalingsindeling Pagamento Fornittori voor leveranciersbetalingen

Verouderde Italiaanse betalingsindeling voor kredietoverdrachten.

|                              |                                                        |
|------------------------------|--------------------------------------------------------|
| Reden voor afschrijving       | De betalingsindeling wordt niet meer gebruikt.                  |
| Vervangen door een andere functie? | Ja, ISO20022-betalingsindeling voor kredietoverdracht voor Italië |
| Modules die worden beïnvloed             | Leveranciers                                           |

### <a name="payment-export-formats-for-estonia"></a>Opmaak voor betalingsexport voor Estland

De indelingen Telehansa en Teleservice worden gebruikt voor het exporteren van bankbetalingen.

|                              |                                                          |
|------------------------------|----------------------------------------------------------|
| Reden voor afschrijving       | De betalingsindelingen worden niet meer gebruikt.                  |
| Vervangen door een andere functie? | Ja, ISO20022-betalingsindeling voor kredietoverdrachten voor Estland |
| Modules die worden beïnvloed             | Leveranciers                                             |

### <a name="payment-file-archive-for-norway"></a>Betalingsbestandsarchief Noorwegen

Wanneer betalingsbestanden worden gegenereerd, archiveert het bestandarchief automatisch alle bestanden die worden gemaakt, zelfs bestanden die eerder zijn geschreven of gelezen.

|                              |                                                                    |
|------------------------------|--------------------------------------------------------------------|
| Reden voor afschrijving       | Vervangen door een andere functie                                        |
| Vervangen door een andere functie? | Ja, Gearchiveerde taken elektronische rapportage                            |
| Modules die worden beïnvloed             | Leveranciers, Klanten, Organisatiebeheer |

### <a name="payment-import-formats-for-estonia"></a>Betalingsindelingen voor import voor Estland

De indelingen Telehansa en TeleTeenus worden gebruikt voor het importeren van bankbetalingen.

|                              |                                                                                            |
|------------------------------|--------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | De betalingsindelingen worden niet meer gebruikt.                                                    |
| Vervangen door een andere functie? | Nr. De indelingen worden vervangen door ISO 20022-importindelingen voor afschriften in toekomstige versies. |
| Modules die worden beïnvloed             | Klanten                                                                          |

### <a name="performance-management-goal-workflow"></a>Werkstroom doel prestatiebeheer

Prestatiebeheer omvat het beheren van het doel en integratie met beoordelingsgesprekken.

|                              |                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | Prestatiebeheer is opnieuw opgezet en het aantal doelpagina's is verminderd om het proces te vereenvoudigen.                 |
| Vervangen door een andere functie? | Nr. De doelen zijn zichtbaar voor managers via de portal Selfservice manager, en kunnen door de manager worden gewijzigd en weergegeven. |
| Modules die worden beïnvloed             | Human Capital-beheer                                                                                                 |

### <a name="postgirot-and-postgirot-utland-payment-formats-for-sweden"></a>De betalingsindelingen Postgirot en Utland Postgirot van Zweden

De betalingsindelingen Postgirot en Utland Postgirot van Zweden.

|                              |                                                         |
|------------------------------|---------------------------------------------------------|
| Reden voor afschrijving       | De betalingsindelingen worden niet meer gebruikt.                 |
| Vervangen door een andere functie? | Ja, ISO20022-betalingsindeling voor kredietoverdracht voor Zweden |
| Modules die worden beïnvloed             | Leveranciers                                            |

### <a name="radio-frequency-identifier"></a>Radiofrequentie-identificatie

Radio Frequency Identification (RFID) is een gegevensverzamelingstechnologie waarbij elektronische tags worden gebruikt om identificatiegegevens op te slaan en er een reader zonder line-of-sight wordt gebruikt om de identificatiegegevens te lezen.

|                              |                                               |
|------------------------------|-----------------------------------------------|
| Reden voor afschrijving       | Laag klantgebruik en een beperkte functieset. |
| Vervangen door een andere functie? | Nee                                            |
| Modules die worden beïnvloed             | Voorraadbeheer                          |

### <a name="report-about-state-invoices-numbering-for-latvia"></a>Rapport over nummering van verkoopfacturen voor Letland

De Letse wetgeving kent specifieke regels voor het nummeren van verkoopfacturen. Met deze functionaliteit kunt u specifieke nummers toewijzen aan verkoopfacturen, op basis van de gebruiker of gebruikersgroep. U kunt vervolgens een rapport of een XML-bestand genereren. U kunt ook een rapport afdrukken over factuurnummers die worden gebruikt.

|                              |                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | De statusnummering van de factuur hoeft niet meer te worden onderhouden. Het rapport over gebruikte factuurnummers is niet meer nodig. |
| Vervangen door een andere functie? | Nee                                                                                                                       |
| Modules die worden beïnvloed             | Klanten                                                                                                        |

### <a name="set-up-the-names-of-the-manager-and-general-accountant-of-a-company-for-lithuania"></a>De namen van de manager en de algemene boekhouder instellen van een bedrijf voor Litouwen

De namen van de manager en de algemene boekhouder van een bedrijf kunnen in de bedrijfsgegevens zijn opgegeven en in verschillende lokale rapportafdrukken worden gebruikt.

|                              |                                                                 |
|------------------------------|-----------------------------------------------------------------|
| Reden voor afschrijving       | Vervangen door een andere functie                                     |
| Vervangen door een andere functie? | Ja, het instellen van de functionarissen kan voor hetzelfde doel worden gebruikt.   |
| Modules die worden beïnvloed             | Leveranciers, Klanten, Contant- en bankbeheer |

### <a name="telepay-payment-formats-for-norway"></a>Betalingsindelingen voor Telepay voor Noorwegen

De Telepay-betalingsindelingen omvatten export van leveranciersbetalingen (kredietoverdracht) en het innen van klantbetalingen (automatische afschrijving).

|                              |                                                                                                |
|------------------------------|------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | De betalingsindelingen worden niet meer gebruikt.                                                        |
| Vervangen door een andere functie? | Ja, ISO20022-betalingsindeling voor kredietoverdracht en AvtaleGiro-klantbetalingen voor Noorwegen |
| Modules die worden beïnvloed             | Leveranciers, Klanten                                                          |

### <a name="vendor-payment-export-formats-for-finland"></a>Exportindelingen voor leveranciersbetalingen voor Finland

Twee indelingen voor het exporteren van betalingen zijn beschikbaar voor Finland. LM02 (FI) wordt gebruikt voor nationale betalingen en LUM2 (FI) wordt gebruikt voor buitenlandse betalingen.

|                              |                                                          |
|------------------------------|----------------------------------------------------------|
| Reden voor afschrijving       | De betalingsindelingen worden niet meer gebruikt.                  |
| Vervangen door een andere functie? | Ja, ISO20022-betalingsindeling voor kredietoverdracht voor Finland |
| Modules die worden beïnvloed             | Leveranciers                                             |

### <a name="workflow-for-creating-goals"></a>Workflow voor het maken van doelen

Een workflow voor het beheren van het maken van werknemerdoelstellingen is een van meerdere workflows die beschikbaar zijn om het prestatiebeheerproces te coördineren.

|                              |                                                                                                                                                                                                                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | Het prestatiebeheer is volledig opnieuw ontworpen in Microsoft Dynamics 365 for Operations.                                                                                                                                                                                                                                        |
| Vervangen door een andere functie? | De functie Prestatiebeheer is volledig opnieuw ontworpen en geeft meer controle over de inhoud van de doelen, de metingen die worden gebruikt om de voortgang bij te houden en het bijvoegen van ondersteunende documentatie. Doelen kunnen als sjablonen worden opgeslagen en opnieuw worden gebruikt. Deze functie kan u helpen om sneller extra doelen voor uw werknemers op te zetten. |
| Modules die worden beïnvloed             | Human Capital-beheer                                                                                                                                                                                                                                                                                                               |

## <a name="features-deprecated-in-dynamics-ax-70-releases"></a>Functies die zijn verwijderd in Dynamics AX 7.0
### <a name="ability-to-cancel-changes-to-a-vendor-invoice"></a>Mogelijkheid om wijzigingen aan een leveranciersfactuur te annuleren

|                              |                         |
|------------------------------|-------------------------|
| Reden voor afschrijving       | Prestatieverbeteringen |
| Vervangen door een andere functie? | Nee                      |
| Modules die worden beïnvloed             | Leveranciers        |

### <a name="aif-axd-and-axbc-integrations"></a>Integraties met AIF, AxD en AxBC

In Application Integration Framework (AIF) kunnen gegevens worden uitgewisseld met externe systemen door bedrijfslogica die als services beschikbaar is. Dynamics AX bevat services die op documenten en .NET Business Connector (AxBC) zijn gebaseerd. Een document wordt gemaakt door XML te gebruiken. De XML bevat koptekstinformatie die wordt toegevoegd om een *bericht* te maken dat naar of uit Dynamics AX kan worden overgebracht. Voorbeelden van documenten zijn verkooporders en inkooporders. Bijna elke entiteit, zoals een klant, kan echter door een document worden weergegeven. Services die op documenten zijn gebaseerd, gebruiken de **Axd &lt;*Document*&gt;-klassen

|                              |                                                                                                                                                                                                          |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | De architectuur van AIF en AxDs kon niet aan de schaal van een cloudservice worden aangepast. Dit leidde tot prestatieproblemen met de bulkimport.                                                                               |
| Vervangen door een andere functie? | In de huidige versie van Dynamics AX is deze functie vervangen door het raamwerk voor gegevensimport/-export, dat herhalende bulkimport/-export ondersteunt. Voor AxBC is het raadzaam om de werkelijke tabellen te gebruiken. |
| Modules die worden beïnvloed             | AxDs, AxBCs en AIF                                                                                                                                                                                     |

### <a name="boms-without-bom-versions"></a>Stuklijsten zonder stuklijstversies

Wanneer de configuratiesleutel **Stuklijstversies** werd uitgeschakeld, werden de stuklijstversies verborgen in alle formulieren en het systeem dwong een 1:1-relatie af tussen vrijgegeven producten en stuklijsten. In de huidige versie van Dynamics AX kan de configuratiesleutel **Stuklijstversies** niet worden uitgeschakeld.

|                              |                                                                                         |
|------------------------------|-----------------------------------------------------------------------------------------|
| Reden voor afschrijving       | Gebruik van een configuratiesleutel voor controle van de stuklijstversies kon niet worden aangepast aan een cloudomgeving. |
| Vervangen door een andere functie? | Nee                                                                                      |
| Modules die worden beïnvloed             | Productgegevensbeheer, Voorraadbeheer                                    |

### <a name="brazilian-bordero"></a>Braziliaanse Bordero

Specifieke betalingsmethode voor Braziliaanse bedrijven

|                              |                                                                                                       |
|------------------------------|-------------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | De ondersteuning voor de Braziliaanse Bordero-betalingsmethode is verwijderd uit de Braziliaanse lokalisatie |
| Vervangen door een andere functie? | Nee                                                                                                    |
| Modules die worden beïnvloed             | Leveranciers                                                                                          |

### <a name="brazilian-sintegra-statement"></a>Braziliaans Sintegra-overzicht

Federaal belastingoverzicht voor ICMS-belasting

|                              |                                                                                                                       |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | Deze instructie is niet langer geldig in sommige Braziliaanse statussen.                                                     |
| Vervangen door een andere functie? | Nr. Gebruikers kunnen het Algemene elektronische rapportagehulpmiddel (GER) gebruiken om indien nodig het overzicht in specifieke situaties te configureren. |
| Modules die worden beïnvloed             | Belastingboeken                                                                                                          |

### <a name="brazilian-scan-contingency-mode-for-nf-e"></a>Braziliaanse SCAN contingentiemous voor NF-e

(SCAN) wordt gebruikt voor het genereren, exporteren en importeren van de status van een Nota Fiscal eletrônica (NF-e)wanneer de omgeving van Secretaria Da fazenda (SEFAZ) niet beschikbaar is.

|                              |                                                                             |
|------------------------------|-----------------------------------------------------------------------------|
| Reden voor afschrijving       | Deze contingentiemethode is niet langer van toepassing in alle Braziliaanse staten |
| Vervangen door een andere functie? | Nee                                                                          |
| Modules die worden beïnvloed             | Klanten                                                           |

### <a name="business-analyzer"></a>Bedrijfsanalyse

Deze mobiele toepassing laat gebruikers belangrijke zakelijke maatstaven controleren.

|                              |                                                                                                                                                               |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | De functionaliteit is vervangen door een andere functie.                                                                                                      |
| Vervangen door een andere functie? | Het inhoudpakket Financiële prestaties controleren voor Microsoft Power BI bevat belangrijke financiële maatstaven die eerder beschikbaar waren in Business Analyzer. |
| Modules die worden beïnvloed             | Grootboek                                                                                                                                                |

### <a name="business-statistics"></a>Zakelijke statistieken

De instelling van query's voor zakelijke statistieken waarmee u de prestaties van uw organisatie kunt analyseren.

|                              |                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | Verouderde benadering voor Business Intelligence (BI), laag klantgebruik en een beperkte functieset |
| Vervangen door een andere functie? | Nieuwe BI-oplossingen voor de huidige versie van Dynamics AX                                      |
| Modules die worden beïnvloed             | Inkoopbeheer, Leveranciers, Verkoop en marketing, Klanten         |

### <a name="change-document-date-function-in-invoice-approval-journal"></a>Functie voor wijzigen van documentdatum het Factuurgoedkeuringsjournaal

|                              |                                                                         |
|------------------------------|-------------------------------------------------------------------------|
| Reden voor afschrijving       | Laag gebruik                                                               |
| Vervangen door een andere functie? | Ja. De documentdatum op de geboekte leverancierstransactie kan worden gewijzigd. |
| Modules die worden beïnvloed             | Leveranciers                                                        |

### <a name="clieop03-payment-format-for-the-netherlands"></a>Betalingsindeling ClieOp03 voor Nederland

|                              |                                                                                                            |
|------------------------------|------------------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | De indeling is niet meer geldig in Nederland omdat het is vervangen door de functionaliteit voor de gemeenschappelijke betalingsruimte voor de euro (SEPA). |
| Vervangen door een andere functie? | SEPA-betalingen exporteren                                                                                       |
| Modules die worden beïnvloed             | Alles                                                                                                        |

### <a name="compliance-center"></a>Help bij conformiteit

Help bij conformiteit was een site van Enterprise Portal voor het beheren van de documentatiebehoeften voor conformiteitsinitiatieven die verband houden met de Sarbanes Oxley Act.

|                              |                                                                                                                        |
|------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | Gebrek aan klantgebruik. Microsoft SharePoint bevat dezelfde mogelijkheid die in Help bij conformiteit beschikbaar was. |
| Vervangen door een andere functie? | Nee                                                                                                                     |
| Modules die worden beïnvloed             | Conformiteit en interne controles                                                                                       |

### <a name="connector-for-microsoft-dynamics"></a>Connector voor Microsoft Dynamics

Deze tool is gebruikt om belangrijke gegevens van Microsoft Dynamics CRM te integreren in Microsoft Dynamics ERP-toepassingen.

|                              |                                                          |
|------------------------------|----------------------------------------------------------|
| Reden voor afschrijving       | De functionaliteit is vervangen door een andere functie. |
| Vervangen door een andere functie? | Dynamics Integrator                                      |
| Modules die worden beïnvloed             | Connector voor Microsoft Dynamics                         |

### <a name="container-unit-and-multi-dimension-on-hand"></a>Containereenheid en meerdere dimensies voorhanden

|                              |                                                                                                                                                                 |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | Dubbele functionaliteit.                                                                                                                                         |
| Vervangen door een andere functie? | Ja. Sinds AX 2012 is deze functionaliteit vervangen door de geconsolideerde batchorderfunctieset. Deze functieset bevat de geconsolideerde voorhanden weergave. |
| Modules die worden beïnvloed             | Productgegevensbeheer, Productiebeheer, Voorraadbeheer, Verkoop en marketing                                                                   |

### <a name="cue-group-metadata"></a>Metagegevens van hintgroep

|                              |                                                                                                                                                                                                                               |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | De hintgroepen werden gebruikt om één of meer hints in het feitenblokgebied weer te geven. Er was maar weinig gebruik, en er waren ook problemen met de prestaties doordat een recordwijziging in een bovenliggend formulier één query per hint in de hintgroep veroorzaakte. |
| Vervangen door een andere functie? | Nee                                                                                                                                                                                                                            |
| Modules die worden beïnvloed             | Alles                                                                                                                                                                                                                           |

### <a name="cue-metadata"></a>Hint-metagegevens

|                              |                                                                                                                                                                                                                                         |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | De hint-metagegevens zijn beperkt tot gegevens voor som of aantal.                                                                                                                                                                                   |
| Vervangen door een andere functie? | De tegelmetagegevens zijn geïntroduceerd om meer flexibiliteit voor modellering te bieden. U kunt bijvoorbeeld actuele tellingen, navigatie en Key Performance Indicators (KPI's) modelleren. De metagegevens van de tellingstegel zijn de directe vervanging van de hintmetagegevens. |
| Modules die worden beïnvloed             | Alles                                                                                                                                                                                                                                     |

### <a name="danish-check-format"></a>Deense cheque-indeling

|                              |                                                                                                                         |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | Ondersteuning voor de Deense cheque-indeling is beëindigd, en het rapport is verwijderd uit de Deense lokalisatie. |
| Vervangen door een andere functie? | Nee                                                                                                                      |
| Modules die worden beïnvloed             | Alles                                                                                                                     |

### <a name="data-partitions"></a>Gegevenspartities

Gegevenspartities bieden een logische scheiding van gegevens in de Microsoft Dynamics AX-database.

|                              |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | In Microsoft Dynamics AX 2012 R2 werden gegevenspartities geïntroduceerd om de isolatie van gegevens mogelijk te maken. In een gebruikelijk scenario heeft een bedrijf dochterondernemingen en mogen de gegevens van de ene vestiging niet zichtbaar zijn voor een andere vestiging, hoewel beide dochterondernemingen worden beheerd door dezelfde IT-afdeling. Er waren echter extra scripts en beheeroverhead in het hele programma vereist om nieuwe partities maken en deze te vullen met gegevens, en om back-ups van partitiegegevens te maken. In de cloud, waar we toegang hebben tot PaaS-databaseservices (platform als een service) (Microsoft Azure SQL-database), is het veel efficiënter gebruik te maken van een database als de isolatiecontainer dan om isolatie uit te voeren in het programma. Ongeacht of partitioneren van gegevens is vereist voor dochterondernemingen, voor meerdere tenants of gewoon voor schaal, geloven wij dat de scenario's beter kunnen worden verwerkt via meerdere databases of meerdere exemplaren van Dynamics AX. |
| Vervangen door een andere functie? | In een toekomstige versie zullen gegevenspartities worden vervangen via ondersteuning voor meerdere databases of Dynamics AX-exemplaren.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| Modules die worden beïnvloed             | Alles                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |

### <a name="delimitation"></a>Begrenzing

|                              |                                        |
|------------------------------|----------------------------------------|
| Reden voor afschrijving       | Geen gebruik van de functionaliteit gevonden. |
| Vervangen door een andere functie? | Nee                                     |
| Modules die worden beïnvloed             | Tijd en aanwezigheid                    |

### <a name="desktop-client"></a>Bureaubladclient

|                              |                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | De ervaring met de Dynamics AX-client is opnieuw ontworpen om bruikbaarheid over meerdere platformen en apparaten te verbeteren.                      |
| Vervangen door een andere functie? | De nieuwe webclient is gebaseerd op het metagegevens en programmeringsmodel van het bureaubladformulier, die zijn aangepast om een rijk webplatform te bieden. |
| Modules die worden beïnvloed             | Alles                                                                                                                                    |

### <a name="dutch-swift-mt940"></a>Nederlandse SWIFT MT940

|                              |                                                                                                                                                                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | Algemene functionaliteit wordt nu gebruikt in plaats van gelokaliseerde functionaliteit.                                                                                                                                                                 |
| Vervangen door een andere functie? | Ja, deze functionaliteit is vervangen door de functionaliteit Geavanceerde bankafstemming. Daarnaast is de implementatie van de import van het camt.053 ISO20022-rekeningoverzicht gepland voor het algemene journaal in de volgende update van Dynamics AX. |
| Modules die worden beïnvloed             | Alles                                                                                                                                                                                                                                   |

### <a name="ebilanz-xbrl-for-germany"></a>eBilanz (XBRL voor Duitsland)

Deze functionaliteit bood uitvoer in eXtensible Business Reporting Language (XBRL) die voor de Duitse eBilanz-taxonomie is bedoeld.

|                              |                                                                                                                                                                        |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | Gebrek aan klantgebruik                                                                                                                                                 |
| Vervangen door een andere functie? | Deze functie is niet vervangen door een andere functie, maar meerdere gespecialiseerde XBRL-pakketten die uitgebreide XBRL-functionaliteit bieden, zijn beschikbaar voor de Duitse markt. |
| Modules die worden beïnvloed             | Management Reporter                                                                                                                                                    |

### <a name="enterprise-portal-client"></a>Enterprise Portal-client

|                              |                                                                                                                                        |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | Een enkel clientplatform wordt geboden.                                                                                            |
| Vervangen door een andere functie? | De nieuwe webclient is gebaseerd op de metagegevens en het programmeringsmodel van het bureaubladformulier, die zijn aangepast om een rijk webplatform te bieden. |
| Modules die worden beïnvloed             | Alles                                                                                                                                    |

### <a name="environmental-sustainability"></a>Milieuduurzaamheid

|                              |                                                    |
|------------------------------|----------------------------------------------------|
| Reden voor afschrijving       | Laag klantgebruik en een beperkte functieset       |
| Vervangen door een andere functie? | Nee                                                 |
| Modules die worden beïnvloed             | Conformiteit en interne controles, Leveranciers |

### <a name="form-activex-and-managed-host-controls"></a>Besturingselementen in formulier-ActiveX en Managed Host

|                              |                                                                                                                                                                                               |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | De besturingselementen voor ActiveX en de Managed Host zijn gebaseerd op de verouderde bureaubladclient.                                                                                                             |
| Vervangen door een andere functie? | Het uitbreidbare besturingselementraamwerk ondersteunt het maken van nieuwe besturingselementen die op HTML, CSS, en JavaScript zijn gebaseerd, en is een prima besturingselement in de Microsoft Visual Studio Tooling-omgeving. |
| Modules die worden beïnvloed             | Alles                                                                                                                                                                                           |

### <a name="generate-prenotes-by-using-a-batch"></a>Voorafmeldingen genereren door een batch te gebruiken

Het genereren van voorafmeldingen kan niet worden uitgevoerd door een batch te gebruiken, maar kan nog wel door een gebruiker worden gedaan.

|                              |                                                                                                        |
|------------------------------|--------------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | Er bestaat geen formulier om het resulterende voorafmeldingenbestand permanent op te slaan en weer te geven wanneer het wordt gegenereerd door een batch te gebruiken. |
| Vervangen door een andere functie? | Voorafmeldingen kunnen nog steeds worden gegenereerd, en de gebruiker kan bepalen waar het bestand wordt opgeslagen.   |
| Modules die worden beïnvloed             | Leveranciers, Klanten, Contant- en bankbeheer                                        |

### <a name="german-dtaus-payment-export-and-account-statement-import-totals-and-transactions"></a>Duitse DTAUS-betalingsexport en rekeningoverzichtimport (totalen en transacties)

|                              |                                                                                                                                                                                                                                                                                                |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | De indeling is niet meer geldig in Duitsland, omdat het is vervangen door de functionaliteit voor de gemeenschappelijke betalingsruimte voor de euro (SEPA).                                                                                                                                                                 |
| Vervangen door een andere functie? | Ja, deze functionaliteit is vervangen door de functionaliteit voor export van SEPA-betalingen en geavanceerde bankafstemming bij het importeren van rekeningoverzichten. Daarnaast is de implementatie van de import van het camt.053 ISO20022-rekeningoverzicht gepland voor het algemene journaal in de volgende update van Dynamics AX. |
| Modules die worden beïnvloed             | Alles                                                                                                                                                                                                                                                                                            |

### <a name="german-dtazv-payment-format"></a>Indeling van Duitse DTAZV-betalingen

|                              |                                                                                                    |
|------------------------------|----------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | De indeling is niet meer geldig in Duitsland omdat het is vervangen door de functionaliteit voor de gemeenschappelijke betalingsruimte voor de euro (SEPA). |
| Vervangen door een andere functie? | SEPA-betalingen exporteren                                                                               |
| Modules die worden beïnvloed             | Alles                                                                                                |

### <a name="german-mt940-import"></a>Duitse MT940-import

|                              |                                                                                                                                                                                                                                       |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | Algemene functionaliteit wordt nu gebruikt in plaats van gelokaliseerde functionaliteit.                                                                                                                                                                 |
| Vervangen door een andere functie? | Ja, deze functionaliteit is vervangen door de functionaliteit Geavanceerde bankafstemming. Daarnaast is de implementatie van de import van het camt.053 ISO20022-rekeningoverzicht gepland voor het algemene journaal in de volgende update van Dynamics AX. |
| Modules die worden beïnvloed             | Alles                                                                                                                                                                                                                                   |

### <a name="german-xml-eu-sales-list"></a>XML-indeling voor Duitse ICL-lijst

|                              |                                                                                                                                                                                    |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | De XML-indeling voor de rapportage van de Duitse ICL-lijst wordt niet meer ondersteund. Alleen de ELMA5-tekstbestandsindeling kan worden gebruikt om het rapport van de ICL-lijst bij de Duitse belastingdienst in te dienen. |
| Vervangen door een andere functie? | Nee                                                                                                                                                                                 |
| Modules die worden beïnvloed             | Btw                                                                                                                                                                                |

### <a name="gl-ssrs-reports"></a>GL SSRS-rapporten

Rapporten die de volgende menu-items bevatten, zijn verwijderd: **Proefbalans overzicht**, **Gedetailleerde proefbalans**, **Rekeningschema**, **Audittrail**, **Saldi** en **Saldilijst**.

|                              |                                                                                                                                              |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | Financiële rapporten van Microsoft SQL Server Reporting Services (SSRS) zijn vervangen door de mogelijkheden en standaardrapporten van Management Reporter. |
| Vervangen door een andere functie? | Management Reporter (in de huidige versie van Dynamics AX aangeduid als **Financiële rapportage**)                                                  |
| Modules die worden beïnvloed             | Grootboek                                                                                                                               |

### <a name="infopart-and-formpart-metadata"></a>Metagegevens voor InfoPart en FormPart

|                              |                                                                                                                                                                                                                                |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | Metagegevens voor InfoPart en FormPart maakten het mogelijk om feitenblokken voor twee verschillende clients te maken.                                                                                                                                    |
| Vervangen door een andere functie? | De InfoPart-metagegevens, die een vereenvoudigde formulierdefinitie zijn, zijn omgezet in een formulier met upgrade-tooling. De FormPart-metagegevens, die naar een formulier verwezen, zijn vervangen door een directere verwijzing die door upgrade-tooling wordt aangemaakt. |
| Modules die worden beïnvloed             | Alles                                                                                                                                                                                                                            |

### <a name="main-account-list-page"></a>Lijstpagina Hoofdrekening

Een lijst met rekeningen voor de rechtspersoon en de gerelateerde saldogegevens

|                              |                                                                                                                                                                                    |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | Saldoinformatie is beschikbaar op de lijstpagina **Proefbalans** per rekening en dimensie.                                                                                      |
| Vervangen door een andere functie? | **Hoofdrekeningen** bevat dezelfde lijst met rekeningen die de lijstpagina **Hoofdrekening** bevatte. In de rasterweergave ook **Hoofdrekeningen** wordt nog een kleinere, rasterachtige weergave getoond. |
| Modules die worden beïnvloed             | Grootboek                                                                                                                                                                     |

### <a name="malaysia-and-singapore-bank-cash-flow-report"></a>Bankcashflowrapport voor Maleisië en Singapore

Met deze functie kan de gebruiker een cashflowrapport afdrukken waarop de transacties en details van de kasinkomsten en -uitgaven in een bepaald datumbereik worden weergegeven voor geselecteerde bankrekeningen.

|                              |                                                                         |
|------------------------------|-------------------------------------------------------------------------|
| Reden voor afschrijving       | Dezelfde informatie kan uit de query banktransacties worden verkregen. |
| Vervangen door een andere functie? | Banktransactie opvragen                                            |
| Modules die worden beïnvloed             | Contanten en bankbeheer                                                |

### <a name="mexican-cfd-electronic-invoice"></a>Mexicaanse CFD elektronische factuur

Deze functie maakte het mogelijk Mexicaanse elektronische facturen te genereren door de Comprobante Fiscales Digitales-methode (CFD) te gebruiken, waarin het bedrijf de factuur ondertekent door de gerelateerde autorisatie bij de overheid aan te vragen. Deze functie bevat ook een maandelijks rapport dat alle elektronische facturen bevat die zijn uitgegeven in de periode.

|                              |                                                                                                                                                                                                                                                                                                                                                                                                           |
|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | De methode is niet langer van toepassing. Het genereren van elektronische facturen via de CFD-methode is beëindigd door de belastingdienst en vervangen door de methode Comprobante Fiscal Digital a través de Internet (CFDI), waarin het ondertekenen aan de externe provider (PAC)wordt gedelegeerd. Het maandelijkse rapport is verwijderd, en een queryoptie geeft gebruikers de mogelijkheid om historische transacties op te vragen. |
| Vervangen door een andere functie? | Nee                                                                                                                                                                                                                                                                                                                                                                                                        |
| Modules die worden beïnvloed             | Klanten, Project                                                                                                                                                                                                                                                                                                                                                                              |

### <a name="mexico-realized-and-unrealized-vat"></a>Gerealiseerde en niet-gerealiseerde btw voor Mexico

Microsoft Dynamics AX 2012 beheerde niet-gerealiseerde btw door specifiek voor Mexico bedoelde functionaliteit voor "niet-gerealiseerde btw" te gebruiken.

|                              |                                                                                                                     |
|------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | Dubbele functionaliteit.                                                                                             |
| Vervangen door een andere functie? | Ja, deze functionaliteit is vervangen door standaard voorwaardelijke btw-functionaliteit die in het kernsysteem wordt verschaft. |
| Modules die worden beïnvloed             | Btw                                                                                                                 |

### <a name="microsoft-outlook-integration"></a>Microsoft Outlook-integratie

|                              |                                                                                |
|------------------------------|--------------------------------------------------------------------------------|
| Reden voor afschrijving       | Deze functionaliteit is vervangen door Microsoft Exchange Server-integratie. |
| Vervangen door een andere functie? | Ja                                                                            |
| Modules die worden beïnvloed             | Verkoopbeheer en marketing                                                            |

### <a name="payroll-information-in-human-resources"></a>Salarisgegevens in Human Resources

Salarisgegevens in Human Resources

|                              |                                                                                                                                                                                                                                                                                                                              |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | Deze functionaliteit is vervangen door basispagina´s van Salarisadministratie en Human Resources.                                                                                                                                                                                                                                              |
| Vervangen door een andere functie? | **Vergoedingen**, **Inkomsten** en andere gerelateerde pagina's die eerder deel uitmaakten van Salaris VS, zijn opnieuw geconfigureerd en maken nu deel uit van de basisconfiguratie van Human Resources en helpen externe loonlijstverwerking te ondersteunen. Deze functionaliteit is toegankelijk door de configuratiesleutel **Human Resources 1** &gt; **Salaris** te gebruiken. |
| Modules die worden beïnvloed             | Human Resources, Salaris                                                                                                                                                                                                                                                                                                     |

### <a name="private-blocking-of-inventory-and-warehouse-management-journals"></a>Als privé blokkeren van journalen voor voorraad- en magazijnbeheer

De voorraad- en magazijnjournalen ondersteunen niet meer de mogelijkheid om een journaal te markeren als privé voor een geselecteerde gebruiker. Alleen het proces om journalen te blokkeren als privé voor gebruikersgroepen en blokkeren tijdens het bewerken wordt ondersteund.

|                              |                                        |
|------------------------------|----------------------------------------|
| Reden voor afschrijving       | Geen gebruik van de functionaliteit gevonden. |
| Vervangen door een andere functie? | Nee                                     |
| Modules die worden beïnvloed             | Voorraadbeheer                   |

### <a name="product-builder"></a>Product Builder

Product Builder werd gebruikt om dynamisch items te configureren vanuit een verkooporder, inkooporder, productieorder, verkoopofferte, projectofferte of artikelbehoefte. Op basis van een productmodel dat modelvariabelen had, kon de gebruiker waarden selecteren om te voldoen aan klantbehoeften en een unieke productvariant te krijgen die een stuklijst en een route had.

|                              |                                                                                                                                                                                                         |
|------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | Product Builder liet gebruikers X++-code zien en wordt niet ondersteund in de huidige versie van Dynamics AX. Het is verwijderd om dubbele onderhoudsinspanningen te voorkomen in overlappende codebases van aanzienlijke omvang. |
| Vervangen door een andere functie? | Productconfiguratie                                                                                                                                                                                   |
| Modules die worden beïnvloed             | Productiegegevensbeheer, Verkoop en marketing                                                                                                                                                     |

### <a name="rename-product-dimension"></a>Productdimensie hernoemen

Met deze functie kon u de naam van een van de drie standaardproductdimensies (grootte, kleur of stijl) wijzigen in een naam die beter aansloot op uw zakelijke behoeften. Hernoemen omvatte alle labels waar de productdimensienaam werd gebruikt.

|                              |                                                                               |
|------------------------------|-------------------------------------------------------------------------------|
| Reden voor afschrijving       | De huidige versie van Dynamics AX ondersteunt geen labelwijzigingen tijdens runtime. |
| Vervangen door een andere functie? | Nee                                                                            |
| Modules die worden beïnvloed             | Productgegevensbeheer                                                |

### <a name="role-center-pages"></a>Pagina's van rollencentrums

|                              |                                                                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | Rollencentrum-pagina's zijn gebaseerd op het verouderd Enterprise Portal-platform, dat door het nieuwe webclientplatform in de huidige versie van Dynamics AX is vervangen. |
| Vervangen door een andere functie? | Het patroon van het nieuwe Werkruimteformulier biedt gebruikers een proces-gecentreerd ontwerp, dat eenvoudig toegang biedt tot vaak gebruikte taken binnen dat proces.                       |
| Modules die worden beïnvloed             | Alles                                                                                                                                                                      |

### <a name="sales-tax-jurisdictions"></a>Btw-jurisdictie

|                              |                                              |
|------------------------------|----------------------------------------------|
| Reden voor afschrijving       | Laag klantgebruik en een beperkte functieset |
| Vervangen door een andere functie? | Nee                                           |
| Modules die worden beïnvloed             | VS btw                                 |

### <a name="shipping-carrier-interface"></a>Vervoerders interface

|                              |                                                                                                                                                 |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | Dubbele functionaliteit.                                                                                                                         |
| Vervangen door een andere functie? | Ja, deze functie is gedeeltelijk vervangen door Transportbeheer, maar is nog niet vervangen door basismagazijnbeheer (WMS I). |
| Modules die worden beïnvloed             | Verkoop en marketing, Voorraadbeheer                                                                                                       |

### <a name="sites-services"></a>Sites Services

Met Sites Services kunt u websites maken die uw bedrijfsprocessen naar internet uitbreiden zonder IT-ondersteuning.

|                              |                                                                                                                                          |
|------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | De Microsoft Azure-infrastructuur die door Dynamics AX wordt gebruikt, heeft nieuwe mogelijkheden die in plaats daarvan kunnen worden gebruikt (bijvoorbeeld Azure-sites). |
| Vervangen door een andere functie? | Nee                                                                                                                                       |
| Modules die worden beïnvloed             | HR-werving, Aanvraagbeheer, Offerteaanvragen, Leveranciersregistratie                                                                  |

### <a name="ssas-demand-forecasting-strategy"></a>SSAS-vraagprognosestrategie

|                              |                                                                              |
|------------------------------|------------------------------------------------------------------------------|
| Reden voor afschrijving       | Het ontwerp van de functie kan niet worden ondersteund in de nieuwe cloudarchitectuur. |
| Vervangen door een andere functie? | Azure Machine Learning-vraagprognosestrategie                           |
| Modules die worden beïnvloed             | Planning                                                                     |

### <a name="travel-requisitions"></a>Reisaanvragen

|                              |                                                                 |
|------------------------------|-----------------------------------------------------------------|
| Reden voor afschrijving       | Laag gebruik en de meeste functionaliteit maakte deel uit van Enterprise Portal. |
| Vervangen door een andere functie? | Nee                                                              |
| Modules die worden beïnvloed             | Onkostenbeheer                                              |

### <a name="vendor-invoice-pool-excluding-posting-details"></a>Leveranciersfactuurpool met uitzondering van boekingsdetails

|                              |                                                                                                         |
|------------------------------|---------------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | Laag gebruik. Deze functionaliteit is vervangen door het factuurjournaal dat workflowfunctionaliteit heeft. |
| Vervangen door een andere functie? | Workflowmogelijkheden van het factuurjournaal.                                                           |
| Modules die worden beïnvloed             | Leveranciers                                                                                        |

### <a name="virtual-company-accounts"></a>Virtuele bedrijfsrekeningen

De functie voor virtuele bedrijven wordt niet meer ondersteund in Dynamics AX. Met de functie Virtuele konden gebruikers tabellen instellen die konden worden gedeeld door een reeks bedrijven. Zie voor een omschrijving van de functie [Bedrijfsrekeningen en virtuele bedrijfsrekeningen](https://msdn.microsoft.com/en-us/library/aa834382(v=ax.10).aspx). De functie werkt door tabellen in verzamelingen te groeperen die aan virtuele bedrijven zijn toegewezen, die groepen van bestaande "echte" bedrijven zijn. Query's worden gemaakt zodat alle bedrijven in het virtuele bedrijf toegang hebben tot de gegevens in de tabellen van de gekoppelde tabelverzamelingen.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Reden voor afschrijving</td>
<td><ul>
<li>Virtuele bedrijven moet worden ingericht voordat gegevens in de tabellen worden opgeslagen. Retroactief invoegen van virtuele bedrijven in een bestaande implementatie is zeer moeilijk.</li>
<li>Omdat er zo veel gegevensnormalisatie in de huidige versie van Microsoft Dynamics AX is doorgevoerd, is het lastig geworden om te weten wat aan de tabelverzamelingen moet worden toegevoegd. Het is bijvoorbeeld moeilijk te bepalen welke tabellen moeten worden gedeeld. Alle tabellen waarnaar wordt verwezen vanuit tabellen die deel uitmaken van een virtueel bedrijf, moeten ook worden toegevoegd. Vanwege tabelnormalisatie moeten zelfs eenvoudige hoofdgegevens die zijn verdeeld over meerdere tabellen, deel uitmaken van het virtuele bedrijf. Eventuele fouten die hier worden gemaakt, leiden tot functionele problemen.</li>
<li>Wanneer een tabel deel uitmaakt van een virtueel bedrijf, verliest het informatie over de oorsprong van de gegevens en wordt alleen het virtuele bedrijf geregistreerd.</li>
</ul></td>
</tr>
<tr class="even">
<td>Vervangen door een andere functie?</td>
<td>Algemene tabellen kunnen worden gebruikt om tabellen toegankelijk te maken vanuit alle bedrijven. Momenteel is er geen vervanging.</td>
</tr>
<tr class="odd">
<td>Modules die worden beïnvloed</td>
<td>Niet van toepassing</td>
</tr>
</tbody>
</table>

### <a name="warehouse-management-ii"></a>Magazijnbeheer II

|                              |                                                                                                                                                                                                                                                                                                             |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | De oplossing Magazijnbeheer II (WMS II) die beschikbaar was in de module **Voorraadbeheer** dupliceert functionaliteit in de module **Magazijnbeheer** die is gepubliceerd in Microsoft Dynamics AX 2012 R3.                                                                         |
| Vervangen door een andere functie? | De module **Magazijnbeheer** die is gepubliceerd in AX 2012 R3, Microsoft Dynamics AX 2012 R3 CU8 en Dynamics AX 2012 R3 CU9 vervangt de functies van Magazijnbeheer II De nieuwe module heeft meer geavanceerde functies en flexibelere magazijnbeheerprocessen dan Magazijnbeheer II. |
| Modules die worden beïnvloed             | Voorraadbeheer, Verkoop en marketing, Inkoop en sourcing                                                                                                                                                                                                                                         |

### <a name="worker-reminders-in-human-resources"></a>Herinneringen voor werknemers in Human Resources

Salarisgegevens in Human Resources

|                              |                 |
|------------------------------|-----------------|
| Reden voor afschrijving       | Laag gebruik       |
| Vervangen door een andere functie? | Nee              |
| Modules die worden beïnvloed             | Human resources |

### <a name="workplanner"></a>Werkplanner

|                              |                                                                                                                                                                      |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | Laag gebruik                                                                                                                                                            |
| Vervangen door een andere functie? | Nee, maar de pagina **Profielrelatie** die wordt geopend via de pagina **Profielgroepen** ondersteunt hetzelfde bedrijfsscenario als de afgeschafte pagina **Werkplanner**. |
| Modules die worden beïnvloed             | Tijd en aanwezigheid                                                                                                                                                  |

### <a name="x-financial-statements"></a>X++ in financiële overzichten

|                              |                                                                                             |
|------------------------------|---------------------------------------------------------------------------------------------|
| Reden voor afschrijving       | De functionaliteit is vervangen door een andere functie.                                    |
| Vervangen door een andere functie? | Management Reporter (in de huidige versie van Dynamics AX aangeduid als **Financiële rapportage**) |
| Modules die worden beïnvloed             | Grootboek                                                                              |




