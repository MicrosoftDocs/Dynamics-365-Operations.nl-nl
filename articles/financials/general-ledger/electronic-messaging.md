---
title: Elektronische berichten
description: Dit onderwerp biedt een overzicht en informatie over instellingen voor elektronische berichten in Microsoft Dynamics 365 for Finance and Operations.
author: ShylaThompson
manager: AnnBe
ms.date: 11/16/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.1
ms.translationtype: HT
ms.sourcegitcommit: 232398a6c4193d0074881e26fff361deb9784bf2
ms.openlocfilehash: 082ad886f40a52457900523f44158da3ed939458
ms.contentlocale: nl-nl
ms.lasthandoff: 12/04/2018

---

# <a name="electronic-messaging"></a>Elektronische berichten

[!include [banner](../includes/banner.md)]

Dit onderwerp biedt een overzicht en informatie over instellingen voor elektronische berichten in Microsoft Dynamics 365 for Finance and Operations.

De overheden en wetgevende instanties van verschillende landen en regio's wereldwijd hebben onlang rapportagevereisten geïmplementeerd voor bedrijven die in deze landen of regio's zijn geregistreerd. Het doel van de vereisten is ervoor zorgen dat gegevens in elektronische indeling van die bedrijven worden verkregen, rechtstreeks van de systemen waarin deze zijn berekend, opgeslagen en verwerkt.

De functionaliteit Elektronische berichten in Finance and Operations ondersteunt diverse processen voor elektronische interactie tussen Finance and Operations en de systemen die overheden en wetgevende instanties bieden voor het rapporteren, indienen en ontvangen van officiële informatie.

De functionaliteit Elektronische berichten is geïntegreerd met de module **Elektronische rapportage** (ER). Daarom kunt u twee ER-indelingen voor elektronische berichten instellen. Zie [Elektronische rapportage](https://docs.microsoft.com/en-us/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting) voor meer informatie.

Elektronische berichten is gebaseerd op de volgende entiteiten:

- **Elektronisch bericht**: een rapport dat of aangifte die intern moet worden gerapporteerd en/of verzonden. Een voorbeeld is een rapport dat wordt verzonden naar een btw-kantoor.
- **Items elektronisch bericht**: records die moeten worden opgenomen in het bericht dat wordt gerapporteerd.
- **Elektronische berichtverwerking**: een reeks acties, al dan niet gekoppeld, die moeten worden uitgevoerd om de vereiste gegevens te verzamelen, rapporten te genereren, gegevens op te slaan in Microsoft Azure-blobopslag, rapporten buiten het systeem om te verzenden, antwoorden van buiten het systeem te ontvangen en de database bij te werken, op basis van de ontvangen gegevens.

In de volgende afbeelding wordt de stroom gegevens voor elektronische berichten weergegeven.

![Gegevensstroom voor elektronische berichten](media/electronic-messaging-data-flow.png)

De functionaliteit Elektronische berichten ondersteunt de volgende scenario's:

- Handmatig berichten maken en rapporten genereren die zijn gebaseerd op bijbehorende ER-exportindelingen van verschillende typen: Microsoft Excel, XML, JavaScript Object Notation (JSON), PDF, tekst en Microsoft Word.
- Automatisch berichten maken en verwerken die zijn gebaseerd op informatie die is aangevraagd en verkregen van een dienst via een bijbehorende ER-importindeling.
- Gegevens als berichtitems verzamelen en verwerken vanuit een gegevensbron (Finance and Operations-tabel).
- Aanvullende informatie opslaan en verschillende waarden evalueren door speciaal gedefinieerde uitvoerbare klassen met betrekking tot berichten en berichtartikelen aan te roepen.
- Gegevens samenvoegen die worden verzameld in de berichtitems, die gegevens naar bericht opsplitsen en rapporten genereren in bijbehorende ER-uitvoerindelingen.
- Rapporten verzenden die naar een webservice zijn gegenereerd op basis van de beveiligingsgegevens die zijn opgeslagen in Azure Key Vault.
- Antwoord krijgen van een webservice, het antwoord interpreteren en gegevens bijwerken in Finance and Operations.
- Alle gegenereerde rapporten opslaan en controleren.
- Opslaan en controleren van alle logboekgegevens die betrekking hebben op acties die worden uitgevoerd voor een bericht of berichtitem.
- De verwerking door verschillende berichtstatussen en berichtitemstatussen beheren.

## <a name="set-up-electronic-messaging"></a>Elektronische berichten instellen

Met Elektronische berichten kunt u verschillende elektronische rapportageprocessen voor verschillende documenttypen onderhouden. In sommige complexe scenario's worden elektronische berichten ingesteld om een combinatie van veel berichtstatussen, berichtitemstatussen, acties, extra velden en uitvoerbare klassen te hebben. Voor deze scenario's zijn pakketten met gegevensentiteiten beschikbaar voor import. Als u de pakketten met gegevensentiteiten wilt gebruiken, moet u deze naar een rechtspersoon importeren met behulp van het hulpprogramma Gegevensbeheer. Zie [Gegevensbeheer](../../dev-itpro/data-entities/data-entities-data-packages.md) voor meer informatie over het gebruik van het hulpprogramma Gegevensbeheer.

Als u een pakket met gegevensentiteiten niet importeert, kunt u de functionaliteit Elektronische berichten handmatig instellen. In dat geval moet u de volgende onderdelen instellen: 

- [Nummerreeksen](#number-sequences)
- [Typen en statussen van berichtitems](#message-item-types-and-statuses)
- [Berichtstatussen](#message-statuses)
- [Aanvullende velden](#additional-fields)
- [Uitvoerbare klasse-instellingen](#executable-class-settings)
- [Acties voor invullen van record](#populate-records-actions)
- [Instellingen webservice](#web-service-settings)
- [Acties berichtverwerking](#message-processing-actions)
- [Elektronisch bericht verwerken](#electronic-message-processing)

De volgende secties bevatten meer informatie over elk van deze onderdelen.

### <a name="number-sequences"></a>Nummerreeksen

Stel nummerreeksen in voor berichten en berichtitems. De nummerreeksen worden gebruikt om de berichten en berichtitems automatisch te nummeren. De toegewezen nummers worden gebruikt als unieke id's voor de berichten en berichtitems in het systeem. U kunt nummerreeksen voor elektronische berichten instellen op de pagina **Grootboekparameters** (**Grootboek** \> **Grootboek instellen** \> **Grootboekparameters**).

### <a name="message-item-types-and-statuses"></a>Typen en statussen van berichtitems

Met berichtitemtypen worden recordtypen aangeduid die worden gebruikt in elektronische berichten. U kunt berichtitemtypen instellen op de pagina **Typen berichtitems** (**Belasting** \> **Instellingen** \> **Elektronische berichten** \> **Typen berichtitems**).

Met berichtitemstatussen worden de statussen aangeduid die van toepassing zijn op berichtitems in de verwerking die u instelt. U kunt berichtitemtypen instellen op de pagina **Statussen berichtitem** (**Belasting** \> **Instellingen** \> **Elektronische berichten** \> **Statussen berichtitem**).

### <a name="message-statuses"></a>Berichtstatussen

Stel de berichtstatussen in die beschikbaar moeten zijn in de berichtverwerking. U kunt berichtitemstatussen instellen op de pagina **Berichtstatussen** (**Belasting** \> **Instellingen** \> **Elektronische berichten** \> **Berichtstatussen**).

### <a name="additional-fields"></a>Aanvullende velden

Met de functionaliteit Elektronische berichten kunt u records uit een transactietabel vullen. Op deze manier kunt u de records voorbereiden voor rapportage en deze vervolgens rapporteren. Soms bevat de transactietabel niet voldoende gegevens voor de rapportage van een record op basis van de rapportvereisten. U kunt alle gegevens invullen die moeten worden gerapporteerd voor een record door extra velden in te stellen. Extra velden kunnen zowel aan berichten als aan berichtitems worden gekoppeld. U kunt extra velden instellen op de pagina **Extra velden** (**Belasting** \> **Instellingen** \> **Elektronische berichten** \> **Aanvullende velden**).

In de volgende tabel worden de velden op de pagina **Aanvullende velden** beschreven.

| Veld                | Omschrijving |
|----------------------|-------------|
| Veldnaam           | Voer de naam in van een extra kenmerk van berichtitems die gerelateerd zijn aan het proces. Deze naam wordt weergegeven in de gebruikersinterface terwijl u met het proces werkt. De naam kan ook worden gebruikt in ER-configuraties die zijn gerelateerd aan het proces. |
| Omschrijving          | Voer een omschrijving in van de extra kenmerk van berichtitems die gerelateerd zijn aan het proces. |
| Veldwaarde          | Voer de veldwaarde in die tijdens rapportage moet worden gebruikt voor een berichtitem. |
| Veldomschrijving    | Voer een omschrijving van de veldwaarde in die tijdens rapportage moet worden gebruikt voor een berichtitem. |
| Rekeningtype         | Enkele extra veldwaarden kunnen worden beperkt tot bepaalde rekeningtypen. Selecteer een van de volgende waarden: **Alle**, **Klant** of **Leverancier**. |
| Rekeningcode         | Als u **Klant** of **Leverancier** hebt geselecteerd in het veld **Rekeningtype**, kunt u het gebruik van veldwaarden verder beperken tot een specifieke groep of tabel. |
| Rekening/groepsnummer | Als u **Klant** of **Leverancier** in het veld **Rekeningtype** hebt geselecteerd en een groep of tabel in het veld **Rekeningcode** hebt ingevoerd, kunt u een specifieke groep of vertegenwoordiger in dit veld opgeven. |
| Geldig vanaf            | Geef de begindatum voor de waarde op. |
| Vervaldatum           | Geef de einddatum voor de waarde op. |

### <a name="executable-class-settings"></a>Uitvoerbare klasse-instellingen

Een uitvoerbare klasse is een X++-methode of -klasse die bij de verwerking van elektronische berichten kan worden aangeroepen in verband met een actie als er evaluatie nodig is voor het proces.

U kunt een uitvoerbaar klasse handmatig instellen op de pagina **Uitvoerbare klasse-instellingen** pagina (**Belasting** \> **Instellingen** \> **Elektronische berichten** \> **Uitvoerbare klasse-instellingen**). Maak een regel en stel de volgende velden in.

| Veld                 | Omschrijving |
|-----------------------|-------------|
| Uitvoerbare klasse      | Voer de naam in die wordt gebruikt tijdens het instellen van een berichtverwerkingsactie waarvoor deze klasse wordt aangeroepen. |
| Omschrijving           | Voer een omschrijving van de uitvoerbare klasse in. |
| Naam uitvoerbare klasse | Selecteer een uitvoerbare X++-klasse. |
| Uitvoeringsniveau       | Dit veld wordt automatisch ingesteld omdat de waarde vooraf moet worden gedefinieerd voor de geselecteerde uitvoerbare klasse. Met dit veld beperkt u op welk niveau de gerelateerde evaluatie wordt uitgevoerd. |
| Klassenomschrijving     | Dit veld wordt automatisch ingesteld omdat de waarde vooraf moet worden gedefinieerd voor de geselecteerde uitvoerbare klasse. |

### <a name="populate-records-actions"></a>Acties voor invullen van record

U gebruikt Acties voor invullen van record om acties in te stellen waarmee records worden toegevoegd aan de tabel Berichtitems en deze kunnen worden toegevoegd aan een elektronisch bericht. Als uw elektronische bericht bijvoorbeeld klantfacturen moet rapporteren, moet u een actie **Records invullen** instellen die is gekoppeld in de tabel **Klantfacturenjournaal** (in het veld **Gegevensbron**). U kunt acties voor het invullen van records instellen op de pagina **Actie voor invullen van record** (**Belasting** \> **Instellingen** \> **Elektronische berichten** \> **Acties voor invullen van record**). Maak een nieuwe record voor elke actie waarmee records moeten worden toegevoegd aan de tabel en stel de volgende velden in.

| Veld       | Omschrijving                                                               |
|-------------|---------------------------------------------------------------------------|
| Naam        | Voer een naam in voor de actie waarmee records in uw proces worden ingevuld.       |
| Omschrijving | Voer een omschrijving in voor de actie waarmee records in uw proces worden ingevuld. |

Voeg op het sneltabblad **Instelling van gegevensbronnen** een regel toe voor elke gegevensbron die wordt gebruikt voor het proces en stel de volgende velden in.

| Veld                  | Omschrijving |
|------------------------|-------------|
| Naam                   | Voer een naam in voor de gegevensbron. |
| Type berichtitem      | Selecteer het type berichtitem dat moet worden gebruikt wanneer records worden gemaakt voor de gegevensbron. |
| Rekeningtype           | Selecteer het type rekening dat moet worden gekoppeld aan records uit de gegevensbron. |
| Naam van hoofdtabel      | Selecteer de tabel in Finance and Operations die een gegevensbron moet zijn. |
| Veld met documentnummer  | Selecteer het veld waaruit het documentnummer moet worden gehaald in de geselecteerde tabel. |
| Veld met documentdatum    | Selecteer het veld waaruit de documentdatum moet worden gehaald in de geselecteerde tabel. |
| Accountveld van document | Selecteer het veld waaruit de documentaccount moet worden gehaald in de geselecteerde tabel. |
| Gebruikersquery             | Als dit selectievakje is ingeschakeld, kunt u een query instellen door **Query bewerken** boven het raster te selecteren. Anders worden alle records ingevuld vanuit de gegevensbron. |

### <a name="web-service-settings"></a>Instellingen webservice

U gebruikt webservice-instellingen om directe gegevensoverdracht naar een webservice in te stellen. U kunt webservice-instellingen instellen op de pagina **Webservice-instellingen** (**Belasting** \> **Instellingen** \> **Elektronische berichten** \> **Webservice-instellingen**).

In de volgende tabel worden de velden op de pagina **Webservice-instellingen** beschreven.

| Veld                   | Omschrijving |
|-------------------------|-------------|
| Webservice             | Geef een naam op voor de webservice. |
| Omschrijving             | Geef een omschrijving van de webservice op. |
| Internetadres        | Geef het internetadres van de webservice op. |
| Getuigschrift             | Selecteer een eerder ingesteld certificaat voor de sleutelkluis. |
| Het antwoordtype – XML | Stel deze optie in op **Ja** als het responstype XML is. |
| Aanvraagmethode          | Geeft aanvraagmethode op. HTTP definieert een set aanvraagmethoden waarmee wordt aangeven welke actie moet worden uitgevoerd voor een bepaalde bron. De methode kan **GET**, **POST** of een andere HTTP-methode zijn. |
| Kopteksten voor aanvraag         | Geef aanvraagkopteksten op. De koptekst van een aanvraag is een HTTP-header die kan worden gebruikt in een HTTP-aanvraag en die niet is gerelateerd aan de inhoud van het bericht. |
| Versleuteling accepteren         | Geef de Accept-Encoding op. De HTTP-header van de Accept-Encoding-aanvraag adverteert de inhoudscodering die de client kan begrijpen. Deze inhoudscodering is meestal een algoritme voor compressie. |
| Inhoudstype            | Geef het inhoudstype op. De entiteitsheader voor Content-Type duidt het materiaaltype van de bron aan. |

### <a name="message-processing-actions"></a>Acties berichtverwerking

U gebruikt berichtverwerkingsacties om acties voor uw processen te maken en de parameters in te stellen. U kunt berichtverwerkingsacties instellen op de pagina **Acties berichtverwerking** (**Belasting** \> **Instellingen** \> **Elektronische berichten** \> **Acties berichtverwerking**).

In de volgende tabellen worden de velden op de pagina **Acties berichtverwerking** beschreven.

#### <a name="general-fasttab"></a>Het sneltabblad Algemeen

| Veld                   | Omschrijving |
|-------------------------|-------------|
| Actietype             | Selecteer het type actie. Zie de sectie [Actietypen voor berichtverwerking](#message-processing-action-types) voor informatie over de beschikbare opties. |
| Indelingstoewijzing          | Selecteer de ER-indeling die voor de actie moet worden aangeroepen. Dit veld is alleen beschikbaar voor acties van het type **Export van elektronische rapportage**, **Import van elektronische rapportage** en **Bericht over export van elektronische rapportage**. |
| Type berichtitem       | Selecteer het recordtype waarvoor de actie moet worden beoordeeld. Dit veld is beschikbaar voor acties van het type **Uitvoeringsniveau berichtitem**, **Export van elektronische rapportage** en **Import van elektronische rapportage** en enkele andere typen. Als u dit veld leeg laat, worden alle gedefinieerde berichtitemtypen voor de berichtverwerking beoordeeld. |
| Uitvoerbare klasse        | Selecteer instellingen voor uitvoerbare klassen die eerder zijn gemaakt. Dit veld is alleen beschikbaar voor acties van het type **Uitvoeringsniveau** **berichtitem**. |
| Actie voor invullen van record | Selecteer een actie voor het invullen van de records die eerder is ingesteld. Dit veld is alleen beschikbaar voor acties van het type **Records invullen**. |

##### <a name="message-processing-action-types"></a>Actietypen voor berichtverwerking

De volgende opties zijn beschikbaar in het veld **Actietype**:

- **Records invullen**: een actie van het type **Records invullen** moet eerder zijn ingesteld. Koppel deze actie aan een actie van het type **Records invullen** zodat deze kan worden verwerkt. Er wordt van uitgegaan dat dit actietype wordt gebruikt voor de eerste actie in de berichtverwerking. Daarom kan alleen een resultaatstatus worden ingesteld voor een actie van dit type. Een beginstatus kan niet worden ingesteld.
- **Bericht maken**: gebruik dit type om gebruikers handmatig te laten maken op de pagina **Elektronische berichten**. Daarom kan geen beginstatus worden ingesteld voor een actie van dit type.
- **Uitvoeringsniveau bericht**: gebruik dit type voor het instellen van een uitvoerbare klasse die moet worden geëvalueerd op het berichtniveau.
- **Uitvoeringsniveau berichtitem**: gebruik dit type voor het instellen van een uitvoerbare klasse die moet worden geëvalueerd op het berichtitemniveau.
- **Export van elektronische rapportage**: gebruik dit type voor acties die een rapport moeten genereren dat is gebaseerd op een ER-exportconfiguratie op berichtitemniveau.
- **Bericht over export van elektronische rapportage**: gebruik dit type voor acties die een rapport moeten genereren dat is gebaseerd op een ER-exportconfiguratie op berichtitemniveau (bijvoorbeeld wanneer een bericht geen berichtitems bevat).
- **Import van elektronische rapportage**: gebruik dit type voor acties die een rapport moeten genereren dat is gebaseerd op een ER-importconfiguratie.
- **Verwerking door gebruiker van berichtniveau**: gebruik dit type voor acties waarbij wordt uitgegaan van enkele handmatige acties door de gebruiker. De gebruiker kan bijvoorbeeld de status van berichten bijwerken.
- **Verwerking door gebruiker**: gebruik dit type voor acties waarbij wordt uitgegaan van een handmatige actie door de gebruiker. De gebruiker kan bijvoorbeeld de status van berichtitems bijwerken.
- **Webservice**: gebruik dit type voor acties waarmee een gegenereerd rapport naar een webservice moet worden verzonden. Dit actietype wordt niet gebruikt voor de communicatie van Italiaanse inkoop- en verkoopfacturen.
- **Aanvraagverificatie**: gebruik dit type om verificatie van een server aan te vragen.

#### <a name="initial-statuses-fasttab"></a>Het sneltabblad Aanvankelijke statussen

> [!NOTE]
> Het sneltabblad **Aanvankelijke statussen** is niet beschikbaar voor acties met als begintype **Records invullen** of **Bericht maken**.

| Veld               | Omschrijving                                                                                         |
|---------------------|-----------------------------------------------------------------------------------------------------|
| Status berichtitem | Selecteer de berichtitemstatus waarvoor de geselecteerde berichtverwerkingsactie moet worden beoordeeld. |
| Omschrijving         | Een omschrijving van de geselecteerde berichtitemstatus.                                                  |

#### <a name="result-statuses-fasttab"></a>Het sneltabblad Resulterende statussen

| Veld               | Omschrijving |
|---------------------|-------------|
| Berichtstatus      | Selecteer de berichtstatussen waarvoor de geselecteerde berichtverwerkingsactie moet worden beoordeeld. Dit veld is alleen beschikbaar voor berichtverwerkingsacties die worden beoordeeld op het berichtniveau. Het veld is bijvoorbeeld beschikbaar voor acties van het type **Export van elektronische rapportage** en **Import van elektronische rapportage**. Het is niet beschikbaar voor acties van het type **Verwerking door gebruiker** en **Uitvoeringsniveau berichtitem**. |
| Omschrijving         | Een omschrijving van de geselecteerde berichtstatus. |
| Antwoordtype       | Het antwoordtype van de geselecteerde berichtstatus. |
| Status berichtitem | Selecteer de resulterende statussen die beschikbaar moeten zijn nadat de geselecteerde berichtverwerkingsactie is beoordeeld. Dit veld is alleen beschikbaar voor berichtverwerkingsacties die worden beoordeeld op het berichtitemniveau. Het is bijvoorbeeld niet beschikbaar voor acties van het type **Verwerking door gebruiker** en **Uitvoeringsniveau berichtitem**. Voor berichtverwerkingsacties die worden beoordeeld op berichtniveau wordt in dit veld de berichtitemstatus weergegeven die is ingesteld voor de geselecteerde berichtstatus. |

### <a name="electronic-message-processing"></a>Elektronisch bericht verwerken

De verwerking van elektronische berichten is een basisconcept van de functionaliteit Elektronische berichten. Hiermee worden acties verzameld die moeten worden beoordeeld voor het elektronische bericht. De acties kunnen worden gekoppeld via een beginstatus en resultaatstatus. Acties van het type **Verwerking door gebruiker** kunnen ook onafhankelijk worden gestart. Op de pagina **Elektronisch bericht verwerken** (**Belasting** \> **Instellingen** \> **Elektronische berichten** \> **Elektronisch bericht verwerken**) kunt u ook extra velden selecteren die moeten worden ondersteund voor de verwerking.

Op het sneltabblad **Actie** kunt u vooraf gedefinieerde acties toevoegen aan de verwerking. U kunt opgeven of een actie afzonderlijk moet worden uitgevoerd of kan worden gestart door de verwerking. (Gebruikersacties moeten afzonderlijk worden uitgevoerd.)

Op het sneltabblad **Aanvullende velden berichtitem** kunt u extra vooraf gedefinieerde velden toevoegen die betrekking hebben op berichtitems. U moet extra velden toevoegen voor elk type berichtitem waarop de velden betrekking hebben.

Op het sneltabblad **Aanvullende velden voor bericht** kunt u extra vooraf gedefinieerde velden toevoegen die betrekking hebben op berichten.

Op het sneltabblad **Beveiligingsrollen** kunt u de beveiligingsrollen instellen die vooraf zijn gedefinieerd in het systeem voor specifieke verwerking. Gebruikers met een specifieke rol zien alleen de verwerking die is gedefinieerd voor die rol.

Op het sneltabblad **Batch** kunt u de verwerking voor een batchregime instellen.

## <a name="work-with-electronic-messages-functionality"></a>Werken met de functionaliteit Elektronische berichten

Als u op berichtniveau werkt, is de pagina **Elektronische berichten** (**Belasting** \> **Query's en rapporten** \> **Elektronische berichten** \> **Elektronische berichten**) geschikter. Als u op het niveau van gegevensverzameling (berichtitem) werkt, is de pagina **Items elektronisch bericht** (**Belasting** \> **Query's en rapporten** \> **Elektronische berichten** \> **Items elektronisch bericht**) geschikter.

### <a name="electronic-messages"></a>Elektronische berichten

Op de pagina **Elektronische berichten** wordt de verwerking weergegeven die voor u beschikbaar is, op basis van uw rol. Beveiligingsrollen worden aan verwerking gekoppeld bij het instellen van die verwerking. Voor elke verwerking die beschikbaar is voor u, worden op de pagina elektronische berichten en gerelateerde gegevens weergegeven.

Op het sneltabblad **Berichten** worden elektronische berichten voor de geselecteerde verwerking weergegeven. Afhankelijk van de status van het geselecteerde bericht en de vooraf gedefinieerde verwerking, kunt u bepaalde acties uitvoeren door de knoppen boven het raster te selecteren:

- **Nieuw**: deze knop is gekoppeld aan acties van het type **Bericht maken**.
- **Verwijderen**: deze knop is beschikbaar als het selectievakje **Verwijderen toestaan** is ingeschakeld voor de huidige status van het geselecteerde bericht.
- **Rapport genereren**: deze knop is gekoppeld aan acties van het type **Bericht over export van elektronische rapportage**.
- **Rapport verzenden**: deze knop is gekoppeld aan acties van het type **Webservice**.
- **Status bijwerken**: deze knop is gekoppeld aan acties van het type **Verwerking door gebruiker van berichtniveau**.
- **Berichtitems**: open de pagina **Items elektronisch bericht**.

Het sneltabblad **Actielogboek** bevat informatie over alle acties die zijn uitgevoerd voor het geselecteerde bericht.

Het sneltabblad **Aanvullende velden voor bericht** bevat alle extra velden die zijn gedefinieerd voor berichten in de instellingen voor verwerking. Ook de waarden van deze extra velden worden weergegeven.

Het sneltabblad **Berichtartikelen** bevat alle berichtartikelen die zijn gerelateerd aan het geselecteerde bericht.

U kunt alle bijlagen voor het geselecteerde bericht bekijken. Deze bijlagen zijn rapporten die al zijn gegenereerd en ontvangen. Selecteer het bericht om bijlagen voor te controleren en selecteer de knop **Bijlage** in het actievenster.

![De knop Bijlage](media/attachment-icon.png)

De pagina **Bijlagen** bevat alle bijlagen die zijn gerelateerd aan het bericht. Als u een bestand wilt weergeven, selecteert u dit in de lijst links en selecteert u vervolgens **Openen** in het actievenster.

![De knop Openen](media/open-button.png)

Als u een bijlage wilt controleren die is gerelateerd aan een bepaalde actie die eerder is uitgevoerd voor een bericht, selecteert u het bericht op de pagina **Elektronische berichten** en selecteert u de actie op het sneltabblad **Actielogboek**. Selecteer vervolgens de knop **Bijlage** in het actievenster.

U kunt ook de hele verwerking of alleen een specifieke actie uitvoeren door **Verwerking uitvoeren** in het actievenster te selecteren.

### <a name="electronic-message-items"></a>Items elektronisch bericht

Op de pagina **Items elektronisch bericht** worden alle berichtitems en een logboek van de acties die zijn uitgevoerd voor elk berichtitem weergegeven. Daarnaast worden de extra velden die zijn gedefinieerd voor de berichtitems en de waarden hiervan weergegeven.

In de volgende tabel worden de velden op het tabblad **Berichtitems** beschreven.

<table>
<thead>
<tr>
<th>Veld</th>
<th>Omschrijving</th>
</tr>
</thead>
<tbody>
<tr>
<td>Wordt verwerkt</td>
<td>De naam van de verwerking die is gebruikt om het berichtitem te maken.</td>
</tr>
<tr>
<td>Berichtitem</td>
<td>De ID van het berichtitem. Deze ID wordt automatisch toegewezen op basis van de nummerreeks voor <strong>Berichtitem</strong> die is gedefinieerd op de pagina <strong>Grootboekparameters</strong>.</td>
</tr>
<tr>
<td>Datum berichtitem</td>
<td>De datum waarop het berichtitem is gemaakt.</td>
</tr>
<tr>
<td>Type berichtitem</td>
<td>Het type berichtitem. Er kunnen verschillende soorten berichtitems worden ingesteld voor dezelfde verwerking (bijvoorbeeld <strong>Binnenkomende facturen</strong> en <strong>Uitgaande facturen</strong>). Dit veld kan alleen automatisch worden ingevuld als een factuur wordt toegevoegd aan de tabel Berichtitems.</td>
</tr>
<tr>
<td>Status berichtitem</td>
<td>De werkelijke status van het berichtitem. De beschikbare statussen variëren en zijn afhankelijk van het type berichtitem. Hieronder vindt u enkele voorbeelden:
<ul>
<li><strong>Ingevuld</strong>: er is een record toegevoegd aan de tabel Berichtitems.</li>
<li><strong>Geëvalueerd</strong>: extra kenmerken zijn berekend voor het berichtartikel.</li>
<li><strong>Gerapporteerd</strong>: het berichtitem is toegevoegd aan een rapport.</li>
<li><strong>Uitgesloten</strong>: deze status kan van pas komen als u een aantal berichtitems uit een rapport wilt verwijderen voordat dit wordt geëxporteerd.</li>
</ul>
</td>
</tr>
<tr>
<td>Transmissiedatum</td>
<td>De datum waarop het berichtitem is verzonden voor verwerking waarbij automatisch een gegenereerd rapport buiten het systeem wordt verzonden.</td>
</tr>
<tr>
<td>Documentnummer</td>
<td>Het veld wordt automatisch gevuld op basis van de instellingen voor de actie voor het invullen van records. Dit veld kan alleen automatisch worden ingevuld als een factuur wordt toegevoegd aan de tabel Berichtitems.</td>
</tr>
<tr>
<td>Rekeningnummer</td>
<td>Het rekeningnummer van een klant of leverancier (of een ander veldwaarde, afhankelijk van het veld dat is gedefinieerd voor de actie <strong>Records invullen</strong>). Dit veld kan alleen automatisch worden ingevuld als een factuur wordt toegevoegd aan de tabel Berichtitems.</td>
</tr>
<tr>
<td>Bericht</td>
<td>Het nummer van het bericht. Dit nummer wordt automatisch toegewezen op basis van de nummerreeks voor <strong>Bericht</strong> die is gedefinieerd op de pagina <strong>Grootboekparameters</strong>.</td>
</tr>
<tr>
<td>Berichtstatus</td>
<td>De werkelijke status van het elektronische bericht.</td>
</tr>
<tr>
<td>Volgende actie</td>
<td>De volgende acties die voor de huidige status van het berichtitem kunnen worden gestart.</td>
</tr>
</tbody>
</table>

Op het tabblad **Extra velden** worden de extra velden voor het geselecteerde berichtitem en de bijbehorende waarden weergegeven.

#### <a name="run-processing"></a>Verwerking uitvoeren

Selecteer **Verwerking uitvoeren** in het actievenster om de verwerking voor berichtitems uit te voeren. Als u een bepaalde actie wilt uitvoeren in het dialoogvenster **Verwerking uitvoeren**, stelt u de optie **Actie selecteren** in op **Ja** en selecteert u een actie. Als u de hele verwerking wilt uitvoeren, laat u de optie **Actie selecteren** ingesteld op **Nee**.

#### <a name="generate-report"></a>Rapport genereren

Selecteer **Rapport genereren** in het actievenster om een rapport te genereren. Deze knop is gekoppeld aan acties van het type **Bericht over export van elektronische rapportage**.

#### <a name="update-status"></a>Status bijwerken

Selecteer **Status bijwerken** in het actievenster om de status van een of meer berichtitems bij te werken. Gebruik in het dialoogvenster **Status bijwerken** het sneltabblad **Op te nemen records** om berichtitems te selecteren voor bijwerken. Geef de selectiecriteria correct op omdat berichtitemstatussen worden bijgewerkt volgens deze criteria, de oorspronkelijke status van de geselecteerde actie en de door u instelde waarde voor **Nieuwe status**. Nadat een statusupdate is voltooid, wordt het lastig om te bepalen welke items net zijn bijgewerkt. Daarom is het moeilijk om statusupdates terug te draaien.

#### <a name="electronic-messages"></a>Elektronische berichten

Selecteer **Elektronisch bericht** in het actievenster om een elektronisch bericht te controleren dat is gerelateerd aan het geselecteerde berichtitem.

U kunt ook alle bestanden die met het berichtitem overeenkomen bekijken. Selecteer het veld **Bericht** van het berichtitem of selecteer **Elektronisch bericht** in het actievenster. Selecteer op de pagina **Elektronisch bericht** het bericht waarvoor u een rapport wilt bekijken en selecteer vervolgens de knop **Bijlage** in het actievenster.

![De knop Bijlage](media/attachment-icon.png)

De pagina **Bijlagen** bevat alle bijlagen die zijn gerelateerd aan het bericht. Als u een bestand wilt weergeven, selecteert u dit in de lijst links en selecteert u vervolgens **Openen** in het actievenster.

![De knop Openen](media/open-button.png)

#### <a name="original-document"></a>Oorspronkelijk document

Selecteer **Oorspronkelijk document** in het actievenster om het oorspronkelijke document voor het geselecteerde berichtitem te openen.

## <a name="example"></a>Voorbeeld

Nadat u uw ER-indeling hebt gemaakt, hebt toegewezen aan gegevensbronnen en hebt voltooid, kunt u deze uitvoeren met behulp van het werkgebied **Elektronische rapportage**. Er wordt een rapport gegenereerd dat u lokaal kunt opslaan.

Als u de volgende aspecten van het rapportageproces wilt beheren, moet u de verwerking van elektronische berichten instellen:

- Informatie vastleggen over wie het rapport heeft gegenereerd.
- Vastleggen wanneer het rapport is gegenereerd.
- De rapporten opslaan die zijn gegenereerd voor vorige perioden.

Deze sectie bevat een voorbeeld waarin u ziet hoe u de functionaliteit Elektronische berichten kunt instellen om een proces voor rapportage op te bouwen.

### <a name="set-up-and-run-processing-to-call-a-simple-er-exporting-format-to-generate-an-excel-report"></a>Verwerking instellen en uitvoeren om een eenvoudige ER-exportindeling aan te roepen en een Excel-rapport te genereren

Deze sectie bevat een voorbeeld waarin wordt aangegeven hoe u elektronische berichten kunt instellen om een rapport te genereren dat is gebaseerd op een ER-exportindeling voor Excel. Als u dit voorbeeld wilt volgen, moet u al een ER-exportindeling voor Excel hebben gemaakt, hebben toegewezen aan gegevensbronnen en hebben voltooid. Er moet al een nummerreeks zijn ingesteld voor elektronische berichten.

Bij het samenstellen van de verwerking is het handig om eerst op te geven welke verwerkingsacties en statussen moeten worden ingesteld. In de volgende afbeelding ziet u hoe de verwerking er voor dit voorbeeld uitziet.

![Schema voor verwerking](media/processing-scheme.png)

#### <a name="create-message-statuses"></a>Berichtstatussen maken

1. Ga naar **Belasting \> Instellingen \> Elektronische berichten \> Berichtstatussen**.
2. Maak de volgende berichtstatussen:

    - Nieuw
    - Voorbereid
    - Gegenereerd

    ![Berichtstatussen](media/message-statuses.png)

3. Schakel op de regel voor de status **Nieuw** het selectievakje **Verwijderen toestaan** in om gebruikers in staat te stellen berichten met deze status te verwijderen.

#### <a name="create-additional-fields"></a>Extra velden maken

1. Ga naar **Belasting \> Instellingen \> Elektronische berichten \> Aanvullende velden**.
2. Voeg een extra veld met bijbehorende waarden toe. Hier volgt een voorbeeld.

    ![Aanvullende velden](media/additional-fields.png)

3. Stel de optie **Bewerking door gebruiker** in op **Ja** om gebruikers in staat te stellen het veld te bewerken.

#### <a name="create-message-processing-actions"></a>Berichtverwerkingsacties maken

Voor dit voorbeeld maakt u de volgende acties:

- **Bericht maken**
- **Bijwerken naar Voorbereid**
- **Rapport genereren**
- **Bijwerken naar beginstatus** (optioneel)

1. Ga naar **Belasting \> Instellingen \> Elektronische berichten \> Acties berichtverwerking**.
2. Maak een actie met de naam **Bericht maken**. Op het sneltabblad **Algemeen** selecteert u **Bericht maken** in het veld **Actietype**.
3. Maak een actie met de naam **Bijwerken naar Voorbereid** en stel de volgende velden in:

    - Op het sneltabblad **Algemeen** selecteert u **Verwerking door gebruiker van berichtniveau** in het veld **Actietype**.
    - Selecteer op het sneltabblad **Aanvankelijke statussen** de optie **Nieuw** in het veld **Berichtstatus**.
    - Selecteer op het sneltabblad **Resulterende statussen** de optie **Voorbereid** in het veld **Berichtstatus**. Voer in het veld **Antwoordtype** de waarde **Uitgevoerd** in.

4. Maak een actie met de naam **Rapport genereren** en stel de volgende velden in:

    - Op het sneltabblad **Algemeen** selecteert u **Export van elektronische rapportage** in het veld **Actietype**. Selecteer de ER-exportindeling in het veld **Indelingstoewijzing**. De opties zijn **Excel**, **XML**, **JSON**, **Tekst** en **Overig**.
    - Selecteer op het sneltabblad **Aanvankelijke statussen** de optie **Voorbereid** in het veld **Berichtstatus**.
    - Selecteer op het sneltabblad **Resulterende statussen** de optie **Gegenereerd** in het veld **Berichtstatus**. Voer in het veld **Antwoordtype** de waarde **Uitgevoerd** in.

    ![De actie Rapport genereren](media/generate-report-action.png)

5. Optioneel: als u wilt dat gebruikers een rapport meerdere keren opnieuw kunnen genereren, kunt u een actie **Bijwerken naar beginstatus** maken en de volgende velden instellen:

    - Op het sneltabblad **Algemeen** selecteert u **Verwerking door gebruiker van berichtniveau** in het veld **Actietype**.
    - Selecteer op het sneltabblad **Aanvankelijke statussen** de optie **Gegenereerd** in het veld **Berichtstatus**.
    - Selecteer op het sneltabblad **Resulterende statussen** de optie **Voorbereid** of (en) **Nieuw** in het veld **Berichtstatus**. Voer in het veld **Antwoordtype** de waarde **Uitgevoerd** in.

#### <a name="electronic-message-processing"></a>Elektronisch bericht verwerken

In dit voorbeeld moeten de acties zo worden ingesteld dat ze afzonderlijk worden uitgevoerd. De veronderstelling is dat elke actie wordt geïnitialiseerd door de gebruiker.

1. Ga naar **Belasting \> Instellingen \> Elektronische berichten \> Elektronisch bericht verwerken**.
2. Voeg een record voor uw verwerking en alle eerder gedefinieerde acties en een extra veld toe.
3. Optioneel: geef op het sneltabblad **Beveiligingsrollen** beveiligingsrollen voor de verwerking op om de toegang te beperken tot specifieke rapportage.
4. Ga naar **Belasting \> Query's en rapporten \> Elektronische berichten \> Elektronische berichten**.
5. Selecteer **Nieuw** om een bericht te maken. Vervolgens kunt u datums en een omschrijving toevoegen. U kunt ook de waarde van het extra veld bijwerken.

    ![Een elektronisch bericht maken](media/create-electronic-message.png)

Het raster op het sneltabblad **Actielogboek** wordt automatisch gevuld met alle acties die worden uitgevoerd op het bericht.

U kunt de status van het bericht nu verwijderen of bijwerken. Als u de berichtstatus wilt bijwerken, selecteert u **Status bijwerken** en selecteert u **Voorbereid** in het veld **Nieuwe status**. Selecteer vervolgens **OK**.

![De berichtstatus bijwerken](media/update-status.png)

De berichtstatus wordt bijgewerkt naar **Voorbereid** en u kunt het rapport nu genereren door **Rapport genereren** te selecteren. Het rapport wordt gegenereerd en de berichtstatus en het actielogboek worden bijgewerkt. Als u het gegenereerde rapport wilt weergeven, selecteert u de knop **Bijlage** in het actievenster.

