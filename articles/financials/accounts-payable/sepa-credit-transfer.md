---
title: Overzicht SEPA-kredietoverdracht
description: Dit artikel geeft algemene informatie over ISO 20022-overschrijvingen, waaronder SEPA-overschrijvingen (Single euro Payments Area) en andere elektronische betalingen voor leveranciers. Een SEPA-kredietoverdracht is een specifiek type betaling in euro's van een persoon of bedrijf aan een andere persoon of bedrijf. In dit onderwerp wordt ook beschreven hoe u een kredietoverdrachtbetalingsbestand kunt instellen en verzenden.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: LedgerJournalTransVendInvoice, LedgerJournalTransVendPaym, VendPaymMode
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 11124
ms.assetid: 36b0f870-16d4-4bbb-8da5-e747e69b970d
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 1aa70dea3b0e7056afbdba96f4475c3e7e71f57c
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---

# <a name="sepa-credit-transfer-overview"></a>Overzicht SEPA-kredietoverdracht

[!INCLUDE [banner](../includes/banner.md)]

Dit artikel geeft algemene informatie over ISO 20022-overschrijvingen, waaronder SEPA-overschrijvingen (Single euro Payments Area) en andere elektronische betalingen voor leveranciers. Een SEPA-kredietoverdracht is een specifiek type betaling in euro's van een persoon of bedrijf aan een andere persoon of bedrijf. In dit onderwerp wordt ook beschreven hoe u een kredietoverdrachtbetalingsbestand kunt instellen en verzenden.

## <a name="what-is-a-credit-transfer-message"></a>Wat is een kredietoverdrachtsbericht?
Het kredietoverdrachtbericht is een aanvraag die een initiërende partij (uw bedrijf) verzendt om fondsen van een eigen rekening naar een crediteur over te maken. Er zijn veel land- of regio-specifieke en bank-specifieke implementaties van kredietoverdrachtberichten. Enkele daarvan worden gebruikt in een bepaald land/regio en sommige worden standaarden. Een algemeen aanvaarde internationale standaard is ISO 20022 en het initiatiebericht, zoals kredietoverdracht. In de volgende afbeelding ziet u de relaties en dekking voor geselecteerde kredietoverdrachtberichten 
![Kredietoverdracht](./media/credit-transfer.jpg) Kredietoverdrachtberichten 

## <a name="what-are-iso-20022-and-sepa-payments"></a>Wat zijn ISO 20022- en SEPA-betalingen?
De gemeenschappelijke betalingsruimte voor de euro (SEPA) is ingesteld door de Europese Commissie en dicteert dat alle elektronische betalingen als binnenlands worden beschouwd, ongeacht het land/de regio waar de persoon, het bedrijf of organisatie en de bank zich bevinden. Er is geen verschil tussen nationale en grensoverschrijdende betalingen. De SEPA omvat de 28 lidstaten van de Europese Unie (EU) plus IJsland, Liechtenstein, Noorwegen, Zwitserland, Monaco en San Marino. De SEPA helpt met de opbouw van een markt voor betalingstransacties in de Europese Economische Ruimte (EEA). Uiteindelijk moet SEPA het aantal betaalindelingen verminderen waar banken, bedrijven en personen mee moeten werken. De Europese Commissie vestigde de wettelijke basis voor SEPA-betalingen via de Richtlijn betaaldiensten (PSD, Payment Services Directive). De European Payments Council (EPC) ondersteunt SEPA met de volgende activiteiten:

-   De EPC bepaalt de standaarden voor elektronische SEPA-betalingen met behulp van de ISO 20022 UNIFI (Universal financial industry message scheme) XML-indeling.
-   De EPC ontwikkelt regels en richtlijnen over het afhandelen van eurobetalingen.

De EPC, die bestaat uit Europese banken, ontwikkelt commerciële en technische raamwerken voor SEPA-betaalmiddelen. Er worden drie typen SEPA-betalingen gebruikt:

-   Kredietoverdrachten
-   Automatische afschrijvingen
-   Kaarten

## <a name="what-is-a-sepa-credit-transfer"></a>Wat is een SEPA-kredietoverdracht?
Een SEPA-kredietoverdracht is een betaling van een persoon of bedrijf aan een andere persoon of bedrijf. De betalingen moeten in euro's zijn en moeten het Internationale Bankrekeningnummer (IBAN) en de BIC (Bank Identifier Code) voor beide partijen bevatten De BIC wordt ook wel SWIFT-code genoemd \[Society for Worldwide Interbank Financial Telecommunication SWIFT\]. Bovendien moeten transactiekosten worden gedeeld door de beide partijen. Voor kredietoverdrachten tussen partijen moeten XML-bestanden worden gebruikt die voldoen aan de ISO 20022 betalingsverwerkingsstandaarden en de XML-indeling voldoen, zoals opgegeven door de EPC.

## <a name="how-is-a-credit-transfer-implemented"></a>Hoe wordt een kredietoverdracht uitgevoerd?
De kredietoverdrachtbetalingsindeling voor Europese landen wordt geïmplementeerd door middel van de functionaliteit voor Elektronische Rapportage en Betalingsmethoden in Microsoft Dynamics 365 for Finance and Operations. Enkele kredietoverdrachtindelingen die in andere regio's worden gebruikt, gebruiken nog het oude framework voor betalingen. Er zijn vele andere indelingen beschikbaar, waaronder twaalf ISO 20022-bestandsindelingen voor kredietoverdracht. Deze exportindelingen voldoen aan de XML-standaard ISO 20022 voor SEPA. Zij zijn bedoeld om betalingsoverschrijvingen in andere valuta dan euro te genereren, voor de landen/regio's waar ze worden gebruikt, en betalingen in euro zoals opgegeven in versie 8.2 van het SEPA Credit Transfer Scheme Rulebook dat de EPC uitgeeft. Voordat u kredietoverdrachten kunt uitvoeren, moet u contact opnemen met uw bank om software te krijgen die vereist is voor het uploaden van bestanden voor elektronisch bankieren. U kunt die software gebruiken om de XML-bestanden met betalingsopdrachten naar uw bank over te zetten.

## <a name="what-credit-transfer-formats-are-currently-supported-in-finance-and-operations"></a>Welke indelingen voor kredietoverdracht worden momenteel in Finance and Operations ondersteund?
U moet altijd naar de bibliotheek voor gedeelde activa in Microsoft Dynamics Lifecycle Services (LCS) gaan en de meest recente lijst weergeven met beschikbare bestanden die het activumtype **GER-configuratie** hebben. In de volgende sectie, 'Wat moet ik instellen?' vindt u een koppeling naar het onderwerp met informatie over het maken van een LCS-opslagplaats voor het controleren van de beschikbare configuraties en het importeren van geselecteerde configuraties.

## <a name="what-do-i-have-to-set-up"></a>Wat moet ik instellen?
-   Voordat u kredietoverdrachtbestanden kunt maken, moet tenminste één actieve kredietoverdrachtconfiguratie in uw ER-configuraties worden geïmporteerd. Zie voor instructies het onderwerp [Elektronische rapportageconfiguraties downloaden vanuit Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).
-   Wanneer u betalingsmethoden voor leveranciers configureert, selecteert u het selectievakje **Algemene elektronische rapportage**. Selecteer vervolgens de gewenste kredietoverdrachtindeling (bijvoorbeeld **ISO 20022 Kredietoverdracht**) als exportindelingsconfiguratie.
-   U moet ook de rechtspersoon en bankrekeninggegevens in Finance and Operations instellen.
-   Bankrekeningnummers, IBAN's en soms SWIFT-codes (BIC's) of andere id's zijn vereist om geldige kredietoverdracht betalingen te kunnen maken. Daarom moet u deze instellen voor de bankrekening van de leverancier en de bankrekening van de organisatie die de overdracht aanvraagt.
-   Mogelijk is aanvullende informatie vereist, zoals btw-nummers voor de partijen waarnaar wordt verwezen in het kredietoverdrachtbericht. Deze informatie moet worden ingesteld voor leveranciers en voor de rechtspersoon wanneer daarom wordt gevraagd.
-   Sommige leveranciersbetalingsmethoden, meestal de betalingsmethoden op basis van ISO 20022, kunnen aanvullende instellingen vereisen voor **Codesets van de betalingsindeling**, zoals **Servicetype** = **SLEV**. Deze codes worden gebruikt als extra labels voor betalingstransacties tijdens de verwerking van betalingen. Standaardwaarden van betalingscodes, zoals **Categoriedoel**, **Aansprakelijke voor de kosten**, **Lokaal instrument** en **Serviceniveau** kunnen worden ingesteld op twee plaatsen. De eerste plaats is **Journaalkoptekst voor leveranciersbetalingen** en de tweede is **Betalingsmethoden voor leveranciers**. Bij het maken van regels in een betalingsjournaal, worden de waarden van betalingscodes die zijn ingesteld op de betalingsjournaalkoptekst overgebracht naar een journaalregel. Als ze niet zijn ingesteld, worden de waarden uit Betalingsmethoden gebruikt.

## <a name="what-parameters-are-available-for-generating-credit-transfer-payments"></a>Welke parameters zijn beschikbaar voor het genereren van kredietoverdrachtbetalingen?
De lijst met specifieke parameters is afhankelijk van de indeling van de kredietoverdracht. In de volgende tabel staan de parameters die beschikbaar zijn wanneer u een ISO 20022-kredietoverdrachtbetalingsbestand voor Duitsland in een leveranciersbetalingsjournaal genereert. Met de opties op het tabblad **Op de achtergrond uitvoeren** kunt u betalingen genereren in batchmodus.

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
<li><strong>Strd:</strong> Selecteer deze optie om de gestructureerde indeling te gebruiken wanneer één betalingsregel wordt vereffend met één factuur. Deze optie is niet beschikbaar voor de land-/regiospecifieke exportindelingen voor Frankrijk, Duitsland of Nederland.</li>
<li><strong>Ustrd</strong> - Selecteer deze optie om de ongestructureerde indeling te gebruiken wanneer de betaling wordt vereffend met meerdere facturen. De factuurnummers voor de vereffende facturen worden aaneengeschakeld en als remisegegevens gebruikt. Overeenkomstig de ISO 20022-richtlijnen zijn de ongestructureerde remisegegevens beperkt tot 140 tekens.</li>
</ul></td>
</tr>
<tr class="even">
<td>Aantal facturen</td>
<td>Voer het aantal facturen in waarvoor het rapport <strong>Betalingsadvies</strong> wordt afgedrukt.</td>
</tr>
<tr class="odd">
<td>Volgnummer</td>
<td>Voer een volgnummer invoeren om het bestand te identificeren. Het volgnummer wordt weergegeven op het rapport <strong>Bijbehorende notitie</strong>.</td>
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
Het IBAN-nummer (International Bank Account Number) en de BIC (Bank Identifier Code) worden gebruikt om alle rekeningen in vele landen/regio's over de hele wereld te identificeren. Deze omvatten onder meer de 34 SEPA-landen/-regio's. Voer de BIC in in het veld **SWIFT-code** en de IBAN in het veld **IBAN**. Voor zowel de bankrekening van de crediteur als de bankrekening van de klant bevinden deze velden zich op het sneltabblad **Aanvullende identificatie** op het tabblad **Bankrekening** op de pagina **Bankrekeningen**. Het gebruik van BIC voor SEPA-betalingen wordt niet langer afgedwongen.

## <a name="how-do-i-transmit-a-payment-file-to-the-bank"></a>Hoe verzend ik een betalingsbestand naar de bank?
Wanneer u betalingen genereert, wordt het betalingsbestand gegenereerd, en u wordt gevraagd het vanaf uw webbrowser op te slaan op een beschikbare locatie. De volgende stap is het verzenden van het XML-bestand naar uw bank. Dit proces verschilt van bank tot bank. Volg de instructies van uw bank om de bestanden voor verwerking naar de bank te verzenden.




