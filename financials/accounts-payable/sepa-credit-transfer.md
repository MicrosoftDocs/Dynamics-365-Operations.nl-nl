---
title: Overzicht SEPA-kredietoverdracht
description: Dit artikel bevat algemene informatie over ISO 20022 overschrijvingen, waaronder overschrijvingen Single euro Payments Area (SEPA) en andere elektronische betalingen voor leveranciers. Een SEPA-kredietoverdracht is een specifiek type betaling in euro&quot;s van het ene bedrijf naar een ander bedrijf afzonderlijke en/of afzonderlijke. Het onderwerp wordt ook uitgelegd hoe instellen en verzenden van een betalingsbestand voor kredietoverdrachten maken.
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendInvoice, LedgerJournalTransVendPaym, VendPaymMode
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 11124
ms.assetid: 36b0f870-16d4-4bbb-8da5-e747e69b970d
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 4d6cf88788dcc5e982e509137aa444a020137a5e
ms.openlocfilehash: 848df5e3898f37284d7746c59bff8b38d35ac883
ms.lasthandoff: 03/31/2017


---

# <a name="sepa-credit-transfer-overview"></a>Overzicht SEPA-kredietoverdracht

Dit artikel bevat algemene informatie over ISO 20022 overschrijvingen, waaronder overschrijvingen Single euro Payments Area (SEPA) en andere elektronische betalingen voor leveranciers. Een SEPA-kredietoverdracht is een specifiek type betaling in euro's van het ene bedrijf naar een ander bedrijf afzonderlijke en/of afzonderlijke. Het onderwerp wordt ook uitgelegd hoe instellen en verzenden van een betalingsbestand voor kredietoverdrachten maken.

## <a name="what-is-a-credit-transfer-message"></a>Wat is een bericht credit overboeken?
Het bericht van de overboeking credit is een aanvraag die een initiatief partij (uw bedrijf) verzendt fondsen van een eigen rekening naar een crediteur verplaatsen. Er zijn veel land/regio-specifieke en bank-specifieke implementaties van kredietoverdracht berichten. Een paar hiervan worden gebruikt in een land/regio en sommige standaarden worden steeds. Een algemeen aanvaarde internationale standaarden is ISO 20022 en de inleiding berichten, zoals kredietoverdracht. De volgende afbeelding ziet u de relaties en artikelbehoefteplanning voor geselecteerde creditnota overboeking berichten. 
![Creditering van de overdracht is](./media/credit-transfer.jpg) Credit overboeken berichten\[/bijschrift\] 

## <a name="what-are-iso-20022-and-sepa-payments"></a>Wat zijn ISO 20022 en SEPA-betalingen?
De gemeenschappelijke betalingsruimte voor de euro (SEPA) is ingesteld door de Europese Commissie en dicteert dat alle elektronische betalingen als binnenlands worden beschouwd, ongeacht het land/de regio waar de persoon, het bedrijf of organisatie en de bank zich bevinden. Er is geen verschil tussen de nationale en internationale betalingen. SEPA omvat de 28 lidstaten van de europese Unie (EU), en ook IJsland, Liechtenstein, Noorwegen, Zwitserland, Monaco en San Marino. De SEPA helpt met de opbouw van een markt voor betalingstransacties in de Europese Economische Ruimte (EEA). Uiteindelijk moet SEPA het aantal betaalindelingen verminderen waar banken, bedrijven en personen mee moeten werken. De Europese Commissie vestigde de wettelijke basis voor SEPA-betalingen via de Richtlijn betaaldiensten (PSD, Payment Services Directive). De European Payments Council (EPC) ondersteunt SEPA met de volgende activiteiten:

-   De EPC bepaalt de standaarden voor elektronische SEPA-betalingen met behulp van de ISO 20022 UNIFI (Universal financial industry message scheme) XML-indeling.
-   De EPC ontwikkelt regels en richtlijnen over het afhandelen van eurobetalingen.

De EPC, die bestaat uit Europese banken, ontwikkelt commerciële en technische raamwerken voor SEPA-betaalmiddelen. Er worden drie typen SEPA-betalingen gebruikt:

-   Kredietoverdrachten
-   Automatische afschrijvingen
-   Kaarten

## <a name="what-is-a-sepa-credit-transfer"></a>Wat is een SEPA-kredietoverdracht?
Een SEPA-kredietoverdracht is een betaling van een persoon of bedrijf aan een andere persoon of bedrijf. De betalingen moeten in euro's zijn en moeten het Internationale Bankrekeningnummer (IBAN) en de BIC (Bank Identifier Code) voor beide partijen bevatten (Er wordt ook wel BIC Society for Worldwide Interbank Financial Telecommunication \[SWIFT\] code.) Bovendien moeten transactiekosten worden gedeeld tussen beide partijen. Voor kredietoverdrachten tussen partijen moeten XML-bestanden worden gebruikt die voldoen aan de ISO 20022 betalingsverwerkingsstandaarden en de XML-indeling voldoen, zoals opgegeven door de EPC.

## <a name="how-is-a-credit-transfer-implemented"></a>Hoe wordt een kredietoverdracht geïmplementeerd?
De betalingsindeling voor overboeking van krediet voor europese landen wordt geïmplementeerd met behulp van de elektronische aangifte (ER) en methoden van de functionaliteit van de betaling in Dynamics 365 voor bewerkingen. Een paar credit overboeken indelingen worden gebruikt in andere regio's gebruiken om het kader van oudere betaling. Tussen de vele andere indelingen zijn er twaalf ISO 20022 credit overboeken bestandsindelingen die beschikbaar zijn. Deze indelingen exporteren voldoen aan de standaard XML-SEPA ISO 20022. Zij zijn bedoeld voor niet-ingezetenen betalingsoverschrijvingen om landen/regio's waar ze worden gebruikt en de eurobetalingen die is opgegeven in versie 8.2 van het SEPA Credit overboeken Rulebook voor die is meegeleverd de Epc genereren. Voordat u overschrijvingen implementeren kunt, moet u contact op met uw bank voor de software die vereist is om te uploaden bestanden voor elektronisch bankieren. U gebruikt die software om over te brengen van de XML-bestanden met betalingsopdrachten naar uw bank.

## <a name="what-credit-transfer-formats-are-currently-supported-in-dynamics-365-for-operations"></a>Welke indelingen voor credit-overdracht momenteel in Dynamics 365 voor bewerkingen worden ondersteund?
U moet altijd gaat u naar de bibliotheek met gedeelde elementen op de Microsoft Dynamics Lifecycle services (LCS) en weergeven van de meest recente lijst met beschikbare bestanden die een soort activa **GER configuratie**. De volgende sectie, 'Wat heb ik om in te stellen', bevat een koppeling naar het onderwerp met informatie over het maken van een LCS opslagplaats voor het controleren van de beschikbare configuraties en geselecteerde configuraties importeren.

## <a name="what-do-i-have-to-set-up"></a>Wat moet ik instellen?
-   Voordat u kredietoverdracht bestanden maken kunt, moet ten minste één actieve credit overboeken configuratie worden geïmporteerd in uw Emergency Recovery-configuraties. Zie voor meer informatie [elektronische downloaden rapportage configuraties vanuit Lifecycle Services](https://docs.microsoft.com/en-us/dynamics365/operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).
-   Wanneer u rekeningen te betalen betalingsmethoden configureert, selecteert u de **algemene elektronische aangifte** uit en selecteert u de juiste credit overboeken-indeling (bijvoorbeeld **ISO 20022 kredietoverdracht (AT)**) als de configuratie van een export-indeling.
-   U moet ook de juridische entiteit en de bankrekening van de informatie in Dynamics 365 for Operations instellen.
-   Bankrekeningnummers, IBANs en soms SWIFT-codes (BIC's) of andere-id's zijn vereist om te kunnen maken geldig kredietoverdracht betalingen. Daarom moet u instellen ze voor de bankrekening van leverancier en de bankrekening voor de organisatie die de overdracht aanvraagt.
-   Het is mogelijk aanvullende informatie vereist, zoals belasting toegevoegde waarde (btw)-nummers voor de partijen waarnaar wordt verwezen in het bericht credit overboeken. Deze informatie moet worden ingesteld voor leveranciers en voor de rechtspersoon wanneer daarom wordt gevraagd.
-   Sommige rekeningen te betalen betalingsmethoden, meestal op basis van de ISO 20022: betalingsmethoden, vereisen een aanvullende instellingen voor **betaling indeling codesets**, zoals **type Service** = **SLEV**. Deze codes worden gebruikt als extra labels voor betalingstransacties tijdens de verwerking van betalingen. Standaardwaarden van betaling-codes, zoals **doel van de categorie**, **toeslagen aan toonder**, **lokale instrument** en **Service niveau** kan worden ingesteld op twee plaatsen. De eerste plaats is **rekeningen te betalen Betaling journaalkoptekst** en de tweede is **betalen methoden voor betalingen van rekeningen**. Bij betaling journaal regels te maken en betaling codewaarden instellen voor Betaling journaalkoptekst worden overgeboekt naar een journaalregel, als deze niet instellen, de waarden van de betalingsmethoden zijn gebruikt.

## <a name="what-parameters-are-available-for-generating-credit-transfer-payments"></a>Welke parameters zijn beschikbaar voor het genereren van betalingen van creditnota's overboeking?
De lijst met specifieke parameters is afhankelijk van de indeling van de overdracht credit. De volgende tabel ziet de parameters die beschikbaar zijn wanneer u een ISO 20022 betalingsbestand voor kredietoverdrachten maken voor Duitsland in een journaal met betalingen van leverancier genereren. Met de opties die beschikbaar zijn op de **op de achtergrond uitgevoerd** tabblad kunt u betalingen genereren in batchmodus uitgevoerd.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>Veld</th>
<th>Omschrijving</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Batch boeken</td>
<td>Schakel dit selectievakje in om het batchboekingslabel in het XML-bestand op te nemen.</td>
</tr>
<tr class="even">
<td>Verwerking van datum</td>
<td>Voer de datum in waarop de bank de betalingen moet verwerken.</td>
</tr>
<tr class="odd">
<td>Opmaak</td>
<td>Selecteer de indeling voor remisegegevens, afhankelijk van de vereisten van uw land/regio of bank:
<ul>
<li><strong>Strd</strong> : Selecteer deze optie om het gebruik van de gestructureerde indeling wanneer één betalingsregel wordt vereffend met één factuur. Deze optie is niet beschikbaar voor de van land/regio-specifieke exportindelingen voor Frankrijk, Duitsland of Nederland.</li>
<li><strong>Ustrd</strong> - Selecteer deze optie om de ongestructureerde indeling te gebruiken wanneer de betaling wordt vereffend met meerdere facturen. De factuurnummers voor de vereffende facturen worden aaneengeschakeld en als remisegegevens gebruikt. In overeenstemming met ISO 20022 richtlijnen remise van niet-gestructureerde gegevens zijn beperkt tot 140 tekens.</li>
</ul></td>
</tr>
<tr class="even">
<td>Aantal facturen</td>
<td>Voer het aantal facturen dat de <strong>betalingsadvies</strong> rapport wordt afgedrukt vanuit.</td>
</tr>
<tr class="odd">
<td>Volgnummer</td>
<td>Voer een volgnummer invoeren om het bestand te identificeren. Het volgnummer dat wordt weergegeven op de <strong>bijbehorende notitie</strong> rapport.</td>
</tr>
<tr class="even">
<td>Bijbehorende notitie afdrukken</td>
<td>schakel dit selectievakje in om het rapport <strong>Bijbehorende notitie</strong> af te drukken.</td>
</tr>
<tr class="odd">
<td>Controlerapport afdrukken</td>
<td>schakel dit selectievakje in om een rapport met de betalingsgegevens af te drukken.</td>
</tr>
<tr class="even">
<td>Begeleidend schrijven afdrukken</td>
<td>Schakel dit selectievakje in om het rapport <strong>Betalingsadvies</strong> af te drukken.</td>
</tr>
</tbody>
</table>

## <a name="what-are-ibans-and-bics"></a>Wat zijn IBAN en BIC?
De IBAN-nummer (International Bank Account Number) en Code BIC (Bank Identifier) worden gebruikt om elke rekening in veel landen/regio's wereldwijd te identificeren. Deze omvatten de 34 SEPA landen/regio's. Voer de BIC-code in de **SWIFT-code** veld en de IBAN-code in de **IBAN** veld. Voor de bankrekening van de crediteur en de bankrekening van de klant deze velden bevinden zich op de **extra id** sneltabblad op de **bankrekening** tabblad van de **bankrekeningen** pagina. Het gebruik van BIC voor SEPA-betalingen niet langer wordt afgedwongen.

## <a name="how-do-i-transmit-a-payment-file-to-the-bank"></a>Hoe verzend ik een betalingsbestand naar de bank?
Wanneer u betalingen genereert, wordt het betalingsbestand is gegenereerd en u wordt gevraagd om vanuit uw webbrowser op elke beschikbare locatie opslaan. De volgende stap is het XML-bestand verzenden naar uw bank. Dit proces verschilt van bank tot bank. Volg de instructies van uw bank om de bestanden voor verwerking naar de bank te verzenden.


