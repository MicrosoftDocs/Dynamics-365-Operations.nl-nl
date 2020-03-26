---
title: Elektronische berichten
description: Dit onderwerp biedt overzichts- en instellingsinformatie voor elektronische berichten in Microsoft Dynamics 365 Finance.
author: ShylaThompson
manager: AnnBe
ms.date: 11/16/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2018-10-28
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 000a2861bfc108754860f4090ea34901aee5949e
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092055"
---
# <a name="electronic-messaging"></a>Elektronische berichten

[!include [banner](../includes/banner.md)]

Dit onderwerp biedt overzichts- en instellingsinformatie voor elektronische berichten.

De overheden en wetgevende instanties van verschillende landen en regio's wereldwijd hebben onlang rapportagevereisten geïmplementeerd voor bedrijven die in deze landen of regio's zijn geregistreerd. Het doel van de vereisten is ervoor zorgen dat gegevens in elektronische indeling van die bedrijven worden verkregen, rechtstreeks van de systemen waarin deze zijn berekend, opgeslagen en verwerkt.

De functionaliteit Elektronische berichten in Finance ondersteunt diverse processen voor elektronische interactie tussen Finance en de systemen die overheden en wetgevende instanties bieden voor het rapporteren, indienen en ontvangen van officiële informatie.

De functionaliteit Elektronische berichten is geïntegreerd met de module **Elektronische rapportage** (ER). Daarom kunt u twee ER-indelingen voor elektronische berichten instellen. Zie [Elektronische rapportage](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/analytics/general-electronic-reporting) voor meer informatie.

Elektronische berichten is gebaseerd op de volgende entiteiten:

- **Elektronisch bericht**: een rapport dat of aangifte die intern moet worden gerapporteerd en/of verzonden. Een voorbeeld is een rapport dat wordt verzonden naar een btw-kantoor.
- **Items elektronisch bericht**: records die moeten worden opgenomen in het bericht dat wordt gerapporteerd.
- **Elektronische berichtverwerking**: een reeks acties die moeten worden uitgevoerd om de vereiste gegevens te verzamelen, rapporten te genereren, gegevens op te slaan in Microsoft Azure-blobopslag, rapporten buiten het systeem om te verzenden, antwoorden van buiten het systeem te ontvangen en de database bij te werken, op basis van de ontvangen gegevens. De acties in de keten kunnen gekoppeld of ontkoppeld zijn

In de volgende afbeelding wordt de stroom gegevens voor elektronische berichten weergegeven.

![Gegevensstroom voor elektronische berichten](media/electronic-messaging-data-flow.png)

De functionaliteit Elektronische berichten ondersteunt de volgende scenario's:

- Handmatig berichten maken en rapporten genereren die zijn gebaseerd op bijbehorende ER-exportindelingen van verschillende typen: Microsoft Excel, XML, JavaScript Object Notation (JSON), PDF, tekst en Microsoft Word.
- Automatisch berichten maken en verwerken die zijn gebaseerd op informatie die is aangevraagd en ontvangen van een dienst via een bijbehorende ER-importindeling.
- Gegevens als berichtitems verzamelen en verwerken vanuit een gegevensbron. De gegevensbron voor een Finance-tabel
- Aanvullende informatie opslaan en verschillende waarden evalueren door speciaal gedefinieerde uitvoerbare klassen met betrekking tot berichten en berichtartikelen aan te roepen.
- Gegevens samenvoegen die worden verzameld in de berichtitems, die gegevens naar bericht opsplitsen en rapporten genereren in bijbehorende ER-uitvoerindelingen.
- De rapporten verzenden die naar een webservice zijn gegenereerd op basis van de beveiligingsgegevens die zijn opgeslagen in Azure Key Vault.
- Antwoord ontvangen van een webservice, het antwoord interpreteren en gegevens bijwerken in Finance.
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
- [Webtoepassingen](#web-applications)
- [Instellingen webservice](#web-service-settings)
- [Acties berichtverwerking](#message-processing-actions)
- [Elektronisch bericht verwerken](#electronic-message-processing)

De volgende secties bevatten meer informatie over elk van deze onderdelen.

### <a name="number-sequences"></a>Nummerreeksen

Stel nummerreeksen in voor berichten en berichtitems. De nummerreeksen worden gebruikt voor het automatisch nummeren van de berichten en de berichtitems. De nummers die worden toegewezen, worden gebruikt als unieke id´s voor de berichten en berichtitems in het systeem. U kunt nummerreeksen voor elektronische berichten instellen op de pagina **Grootboekparameters** (**Grootboek** \> **Grootboek instellen** \> **Grootboekparameters**).

### <a name="message-item-types-and-statuses"></a>Typen en statussen van berichtitems

Met berichtitemtypen worden recordtypen aangeduid die worden gebruikt in elektronische berichten. U kunt berichtitemtypen instellen op de pagina **Typen berichtitems** (**Belasting** \> **Instellingen** \> **Elektronische berichten** \> **Typen berichtitems**).

Met berichtitemstatussen worden de statussen aangeduid die van toepassing zijn op berichtitems in de verwerking die u instelt. U kunt berichtitemtypen instellen op de pagina **Statussen berichtitem** (**Belasting** \> **Instellingen** \> **Elektronische berichten** \> **Statussen berichtitem**).

Met de parameter **Verwijderen toestaan** van een berichtitemstatus wordt gedefinieerd of gebruikers berichtitems met deze status kunnen verwijderen op de pagina **Elektronische berichten**  of de pagina **Items elektronisch bericht**.

### <a name="message-statuses"></a>Berichtstatussen

Stel de berichtstatussen in die beschikbaar moeten zijn in de berichtverwerking. U kunt berichtitemstatussen instellen op de pagina **Berichtstatussen** (**Belasting** \> **Instellingen** \> **Elektronische berichten** \> **Berichtstatussen**).

In de volgende tabel worden de velden op de pagina **Berichtstatussen** beschreven.

| Veldnaam          | Beschrijving |
|---------------------|-------------|
| Berichtstatus      | Voer een unieke naam voor de berichtstatus in. Berichtstatussen worden gebruikt om de status van een elektronisch bericht op elk moment aan te geven. De naam die u invoert, wordt weergegeven op de pagina **Elektronische berichten** en in een logboek dat betrekking heeft op elektronische berichten. |
| Beschrijving         | Voer een omschrijving van de berichtstatus in. |
| Antwoordtype       | Selecteer het antwoordtype voor de berichtstatus. Sommige acties in een verwerking kunnen meer dan één antwoordtype produceren. Zo kunnen bijvoorbeeld acties van het type **Webservice** antwoorden produceren van het type **Uitgevoerd** of het type **Technische fout**, afhankelijk van het resultaat van de uitvoering ervan. In dit geval moet u berichtstatussen definiëren voor beide antwoordtypen. Raadpleeg [Actietypen voor berichtverwerking](#message-processing-action-types) voor meer informatie over actietypen en de eraan gerelateerde antwoordtypen. |
| Status berichtitem | De status van een elektronisch bericht moet soms de status van gerelateerde berichtitems beïnvloeden. Selecteer een berichtitemstatus in dit veld om deze te koppelen aan de berichtstatus. |
| Verwijderen toestaan        | Schakel dit selectievakje in als gebruikers elektronische berichten met deze status op de pagina **Elektronische berichten** moeten kunnen verwijderen. |

### <a name="additional-fields"></a>Aanvullende velden

Met de functionaliteit Elektronische berichten kunt u records uit een transactietabel invullen. Op deze manier kunt u de records voorbereiden voor rapportage en deze vervolgens rapporteren. Transactietabellen hebben soms echter onvoldoende gegevens om de records in te vullen op een manier die voldoet aan de rapportagevereisten. Om alle gegevens in te vullen die moeten worden gerapporteerd voor een record, kunt u extra velden instellen. Extra velden kunnen zowel aan berichten als aan berichtitems worden gekoppeld. U kunt extra velden instellen op de pagina **Extra velden** (**Belasting** \> **Instellingen** \> **Elektronische berichten** \> **Aanvullende velden**).

In de volgende tabel worden de algemene velden op de pagina **Aanvullende velden** beschreven.

| Veld       | Beschrijving |
|-------------|-------------|
| Veldnaam  | Voer de naam in van een extra kenmerk van berichtitems die gerelateerd zijn aan het proces. Deze naam wordt weergegeven in de gebruikersinterface (UI) terwijl u met het proces werkt. De naam kan ook worden gebruikt in ER-configuraties die zijn gerelateerd aan het proces. |
| Beschrijving | Voer een omschrijving van het aanvullende veld in. |
| Bewerking door gebruiker   | Stel deze optie in op **Ja** als gebruikers de waarde van het aanvullende veld in de gebruikersinterface moeten kunnen wijzigen. |
| Teller     | Stel deze optie in op **Ja** als het aanvullende veld een nummerreeks in een elektronisch bericht moet bevatten. Waarde van het aanvullende veld wordt automatisch ingevuld tijdens het uitvoeren van een actie van het type **Export van elektronische rapportage**. |
| Verborgen      | Stel deze optie in op **Ja** als het aanvullende veld in de gebruikersinterface moet worden verborgen. |

Elk aanvullend veld kan verschillende waarden voor de verwerking hebben. U definieert deze waarden op het sneltabblad **Waarden**: In de volgende tabel worden de velden beschreven.

| Veld                | Beschrijving |
|----------------------|-------------|
| Veldwaarde          | Voer de veldwaarde in die voor een bericht of berichtitem moet worden gebruikt tijdens rapportage. |
| Beschrijving          | Voer een omschrijving van de veldwaarde in. |
| Rekeningtype         | Sommige veldwaarden kunnen worden beperkt tot bepaalde rekeningtypen. Selecteer een van de volgende waarden: **Alle**, **Klant** of **Leverancier**. |
| Rekeningcode         | Als u **Klant** of **Leverancier** hebt geselecteerd in het veld **Rekeningtype**, kunt u het gebruik van de veldwaarde verder beperken tot een specifieke groep of tabel. |
| Rekening/groepsnummer | Als u **Klant** of **Leverancier** in het veld **Rekeningtype** hebt geselecteerd en een groep of tabel in het veld **Rekeningcode** hebt ingevoerd, kunt u een specifieke groep of vertegenwoordiger in dit veld opgeven. |
| Geldig vanaf            | Geef de begindatum voor de waarde op. |
| Vervaldatum           | Geef de einddatum voor de waarde op. |

Standaard zijn combinaties van criteria die zijn gedefinieerd door de velden **Rekening-/groepsnummer**, **Rekeningcode**, **Ingangsdatum** en **Vervaldatum** niet van invloed op de selectie van waarden voor aanvullende velden. Deze combinaties kunnen echter worden gebruikt in een uitvoerbare klasse om specifieke logica te implementeren waarmee waarden voor aanvullende velden worden berekend.

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

Sommige uitvoerbare klassen kunnen verplichte parameters hebben die moeten worden gedefinieerd voordat de uitvoerbare klasse voor de eerste keer wordt uitgevoerd. Als u deze parameters wilt definiëren, selecteert u **Parameters** in het actievenster, stelt u de velden in het dialoogvenster dat verschijnt in en selecteert u vervolgens **OK**. Het is belangrijk dat u **OK** selecteert. Anders worden de parameters niet opgeslagen in de database en wordt de uitvoerbare klasse niet correct opgeroepen.

### <a name="populate-records-actions"></a>Acties voor invullen van record

U gebruikt Acties voor invullen van record om acties in te stellen waarmee records worden toegevoegd aan de tabel Berichtitems en deze kunnen worden toegevoegd aan een elektronisch bericht. Als uw elektronische bericht bijvoorbeeld klantfacturen moet rapporteren, moet u een actie Records invullen instellen die is gekoppeld aan het veld **Gegevensbron** in de tabel Klantfacturenjournaal. U kunt acties voor het invullen van records instellen op de pagina **Actie voor invullen van record** (**Belasting** \> **Instellingen** \> **Elektronische berichten** \> **Acties voor invullen van record**). Maak een nieuwe record voor elke actie waarmee records moeten worden toegevoegd aan de tabel en stel de volgende velden in.

| Veld       | Beschrijving |
|-------------|-------------|
| Naam        | Voer een naam in voor de actie waarmee records in uw proces worden ingevuld. |
| Beschrijving | Voer een omschrijving van de actie Records invullen in. |

Voeg op het sneltabblad **Instelling van gegevensbronnen** een regel toe voor elke gegevensbron die wordt gebruikt voor het proces en stel de volgende velden in.

| Veld                  | Omschrijving |
|------------------------|-------------|
| Naam                   | Voer een naam in voor de gegevensbron. |
| Type berichtitem      | Selecteer het type berichtitem dat moet worden gebruikt wanneer records worden gemaakt voor de gegevensbron. |
| Rekeningtype           | Selecteer het type rekening dat moet worden gekoppeld aan records uit de gegevensbron. |
| Naam van hoofdtabel      | Selecteer de tabel die een gegevensbron moet zijn. |
| Veld met documentnummer  | Selecteer het veld waaruit het documentnummer moet worden gehaald in de geselecteerde tabel. |
| Veld met documentdatum    | Selecteer het veld waaruit de documentdatum moet worden gehaald in de geselecteerde tabel. |
| Accountveld van document | Selecteer het veld waaruit de documentaccount moet worden gehaald in de geselecteerde tabel. |
| Gebruikersquery             | Als dit selectievakje is ingeschakeld, kunt u een query instellen door **Query bewerken** boven het raster te selecteren. Anders worden alle records ingevuld via de geselecteerde gegevensbron ingevuld. |

### <a name="web-applications"></a>Webtoepassingen

U gebruikt webtoepassingsinstellingen om een webtoepassing in te stellen zodat deze Open Authorizaton (OAuth) 2.0 wordt ondersteund. OAuth is de open standard waarmee gebruikers 'beveiligde gedelegeerde toegang' tot de toepassing namens hen kunnen verlenen zonder dat ze hun toegangsreferenties hoeven te delen. U kunt ook het autorisatieproces doorlopen door een autorisatiecode en toegangstoken op te halen. U kunt webtoepassingsinstellingen instellen op de pagina **Webtoepassingen** (**Belasting** \> **Instellingen** \> **Elektronische berichten** \> **Webtoepassingen**).

In de volgende tabel worden de velden op de pagina **Webtoepassingen** beschreven.

| Veld                        | Beschrijving |
|------------------------------|-------------|
| Toepassingsnaam             | Voer een naam voor de webtoepassing in. |
| Beschrijving                  | Voer een omschrijving van de webtoepassing in. |
| Basis-URL                     | Voer het basisinternetadres van de webtoepassing in. |
| URL-pad van autorisatie       | Geef het pad op dat wordt gebruikt om de URL voor autorisatie samen te stellen. |
| URL-pad van token               | Geef het pad op dat wordt gebruikt om de URL voor het token samen te stellen. |
| Omleidings-URL                 | Voer de omleidings-URL in. |
| Client-ID                    | Voer de client-id van de webtoepassing in. |
| Clientgeheim                | Voer het clientgeheim van de webtoepassing in. |
| Servertoken                 | Voer het servertoken van de webtoepassing in. |
| Indelingstoewijzing voor autorisatie | Selecteer de ER-indeling die wordt gebruikt voor het genereren van de aanvraag voor autorisatie. |
| Token modeltoewijzing importeren   | Selecteer de ER-importmodeltoewijzing die wordt gebruikt voor het opslaan van het toegangstoken. |
| Toegewezen bereik                | Het bereik dat wordt verleend voor aanvragen voor de toepassing. Dit veld wordt automatisch bijgewerkt. |
| Toegangstoken verloopt over  | De resterende tijd voordat het toegangstoken vervalt. | 
| Accepteren                       | Geef de eigenschap **Accepteren** van de webaanvraag op. Voer bijvoorbeeld **application/vnd.hmrc.1.0+json** in. |
| Inhoudstype                 | Geef het inhoudstype op. Voer bijvoorbeeld **application/json** in. |

Bovendien zijn de volgende knoppen beschikbaar in het actievenster van de pagina **Webtoepassingen** ter ondersteuning van het autorisatieproces:

- **Autorisatiecode ophalen**: autorisatie van de webtoepassing initialiseren.
- **Toegangstoken verkrijgen**: ophalen van een toegangstoken initialiseren.
- **Toegangstoken vernieuwen**: een toegangstoken vernieuwen.

Wanneer een toegangstoken voor een webtoepassing in de database van het systeem in gecodeerde vorm is opgeslagen, kan het worden gebruikt voor aanvragen bij een webservice. Om beveiligingsredenen moet het toegangstoken worden beperkt tot beveiligingsrollen die moeten worden toegestaan om deze aanvragen af te handelen. Als gebruikers buiten de beveiligingsgroep een aanvraag proberen af te handelen, ontvangen ze een foutbericht waarin wordt gemeld dat niet via de geselecteerde webtoepassing mogen werken. Als u de beveiligingsrollen wilt instellen die toegang tot het toegangstoken moeten hebben, gebruikt u het sneltabblad **Beveiligingsrollen** op de pagina **Webtoepassingen**. Wanneer er geen beveiligingsrollen zijn gedefinieerd voor een webtoepassing, kan alleen een systeembeheerder via deze webtoepassing werken.

### <a name="web-service-settings"></a>Instellingen webservice

U gebruikt webservice-instellingen om directe gegevensoverdracht naar een webservice in te stellen. U kunt webservice-instellingen instellen op de pagina **Webservice-instellingen** (**Belasting** \> **Instellingen** \> **Elektronische berichten** \> **Webservice-instellingen**).

In de volgende tabel worden de velden op de pagina **Webservice-instellingen** beschreven.

| Veld                          | Omschrijving |
|--------------------------------|-------------|
| Webservice                    | Geef een naam op voor de webservice. |
| Omschrijving                    | Geef een omschrijving van de webservice op. |
| Internetadres               | Geef het internetadres van de webservice op. Als een webtoepassing is opgegeven voor de webservice en als het internetadres van de webservice identiek moet zijn aan het internetadres dat is gedefinieerd voor die webtoepassing, selecteert u **Basis-URL kopiëren**om de basis-URL van de webtoepassing naar dit veld te kopiëren. |
| Getuigschrift                    | Selecteer een eerder ingesteld certificaat voor de sleutelkluis. |
| Webtoepassing                | Selecteer een eerder ingesteld certificaat voor de sleutelkluis. |
| Het antwoordtype – XML        | Stel deze optie in op **Ja** als het responstype XML is. |
| Aanvraagmethode                 | Geeft aanvraagmethode op. HTTP definieert een set aanvraagmethoden waarmee wordt aangeven welke actie moet worden uitgevoerd voor een bepaalde bron. De aanvraagmethode kan **GET**, **POST** of een andere HTTP-methode zijn. |
| Kopteksten voor aanvraag                | Geef aanvraagkopteksten op. De koptekst van een aanvraag is een HTTP-header die kan worden gebruikt in een HTTP-aanvraag en die niet is gerelateerd aan de inhoud van het bericht. |
| Accepteren                         | Geef de eigenschap **Accepteren** van de webaanvraag op. |
| Versleuteling accepteren                | Geef de waarde **Accept-Encoding** op. De HTTP-header van de Accept-Encoding-aanvraag adverteert de inhoudscodering die de client kan begrijpen. Deze inhoudscodering is meestal een algoritme voor compressie. |
| Inhoudstype                   | Geef het inhoudstype op. De HTTP-header van de entiteit Content-Type geeft het mediatype van de resource aan. |
| Geslaagde antwoordcode       | Geef de HTTP-statuscode op waarmee wordt aangegeven dat de aanvraag gelukt is. |
| Indelingstoewijzing van aanvraagkopteksten | Selecteer de ER-indeling die wordt gebruikt voor het genereren van webaanvraagkopteksten. |

### <a name="message-processing-actions"></a>Acties berichtverwerking

U gebruikt berichtverwerkingsacties om acties voor uw processen te maken en de parameters in te stellen. U kunt berichtverwerkingsacties instellen op de pagina **Acties berichtverwerking** (**Belasting** \> **Instellingen** \> **Elektronische berichten** \> **Acties berichtverwerking**).

In de volgende tabellen worden de velden op de pagina **Acties berichtverwerking** beschreven.

#### <a name="general-fasttab"></a>Het sneltabblad Algemeen

| Veld                       | Omschrijving |
|-----------------------------|-------------|
| Actietype                 | Selecteer het type actie. Zie de sectie [Actietypen voor berichtverwerking](#message-processing-action-types) voor informatie over de beschikbare opties. |
| Indelingstoewijzing              | Selecteer de ER-indeling die voor de actie moet worden aangeroepen. Dit veld is alleen beschikbaar voor acties van het type **Export van elektronische rapportage**, **Import van elektronische rapportage** en **Bericht over export van elektronische rapportage**. |
| Indelingstoewijzing voor URL-pad | Selecteer de ER-indeling die voor de actie moet worden aangeroepen. Dit veld is alleen beschikbaar voor acties van het type **Webservice**. Het wordt gebruikt voor het samenstellen van het pad van het URL-adres dat wordt toegevoegd aan het basisinternetadres dat is opgegeven voor de geselecteerde webserver. |
| Type berichtitem           | Selecteer het recordtype waarvoor de actie moet worden beoordeeld. Dit veld is beschikbaar voor acties van het type **Uitvoeringsniveau berichtitem**, **Export van elektronische rapportage**, **Import van elektronische rapportage** en **Webservice** en enkele andere typen. Als u dit veld leeg laat, worden alle gedefinieerde berichtitemtypen voor de berichtverwerking beoordeeld. |
| Uitvoerbare klasse            | Selecteer instellingen voor uitvoerbare klassen die eerder zijn gemaakt. Dit veld is alleen beschikbaar voor acties van het type **Uitvoeringsniveau** **berichtitem**. |
| Actie voor invullen van record     | Selecteer een actie voor het invullen van de records die eerder is ingesteld. Dit veld is alleen beschikbaar voor acties van het type **Records invullen**. |
| Webservice                 | Selecteer een webservice die eerder is ingesteld. Dit veld is alleen beschikbaar voor acties van het type **Webservice**. |
| Bestandsnaam                   | Geef de naam op van het bestand dat het resultaat van de actie is. Dit bestand kan het antwoord zijn van de webserver of het rapport dat wordt gegenereerd. Dit veld is alleen beschikbaar voor acties van het type **Webservice** en **Bericht over export van elektronische rapportage**. |
| Dialoogvenster weergeven                 | Stel deze optie in op **Ja** als een dialoogvenster moet worden weergegeven aan gebruikers voordat een rapport wordt gegenereerd. Dit veld is alleen beschikbaar voor acties van het type **Bericht over export van elektronische rapportage**. |

##### <a name="message-processing-action-types"></a>Actietypen voor berichtverwerking

De volgende opties zijn beschikbaar in het veld **Actietype**:

- **Bericht maken**: gebruik dit actietype om gebruikers handmatig berichten te laten maken op de pagina **Elektronische berichten**. Daarom kan geen beginstatus worden ingesteld voor een actie van dit type.
- **Records invullen**: een actie van het type **Records invullen** moet eerder zijn ingesteld. Koppel dit actietype aan een actie van het type Records invullen zodat die actie in de verwerking wordt opgenomen. Hierbij wordt ervan uitgegaan dat dit actietype wordt gebruikt voor de eerste actie in de berichtverwerking (als er van tevoren geen elektronisch bericht is gemaakt) of als een actie waarbij berichtitems worden toegevoegd aan een eerder gemaakt bericht (door een actie van het type **Bericht maken**). Daarom kan de resultaatstatus voor acties van dit type alleen voor berichtitems worden ingesteld. Een beginstatus kan alleen voor berichten worden ingesteld.
- **Uitvoeringsniveau bericht**: gebruik dit actietype voor het instellen van een uitvoerbare klasse die moet worden geëvalueerd op het berichtniveau.
- **Uitvoeringsniveau berichtitem**: gebruik dit actietype voor het instellen van een uitvoerbare klasse die moet worden geëvalueerd op het berichtitemniveau.
- **Export van elektronische rapportage**: gebruik dit actietype voor acties die een rapport moeten genereren dat is gebaseerd op een ER-exportconfiguratie op berichtitemniveau.
- **Bericht over export van elektronische rapportage**: gebruik dit actietype voor acties die een rapport moeten genereren dat is gebaseerd op een ER-exportconfiguratie op berichtitemniveau (bijvoorbeeld wanneer een bericht geen berichtitems bevat).
- **Import van elektronische rapportage**: gebruik dit actietype voor acties die een rapport moeten genereren dat is gebaseerd op een ER-importconfiguratie.
- **Verwerking door gebruiker van berichtniveau**: gebruik dit actietype voor acties waarbij wordt uitgegaan van enkele handmatige acties door de gebruiker op berichtniveau. De gebruiker kan bijvoorbeeld de status van berichten bijwerken.
- **Verwerking door gebruiker**: gebruik dit actietype voor acties waarbij wordt uitgegaan van enkele handmatige acties door de gebruiker op berichtitemniveau. De gebruiker kan bijvoorbeeld de status van berichtitems bijwerken.
- **Webservice**: gebruik dit actietype voor acties waarmee een gegenereerd rapport naar een webservice moet worden verzonden. Dit actietype wordt niet gebruikt voor de communicatie van Italiaanse inkoop- en verkoopfacturen. Voor acties van het type **Webservice** kunt u een bevestigingstekst op het sneltabblad **Overige details** van **Acties berichtverwerking** opgeven. Deze bevestigingstekst wordt weergegeven aan gebruikers voordat aanvragen aan de geselecteerde webservice worden gericht.
- **Aanvraagverificatie**: gebruik dit actietype om verificatie van een server aan te vragen.

#### <a name="initial-statuses-fasttab"></a>Het sneltabblad Aanvankelijke statussen

> [!NOTE]
> Het sneltabblad **Aanvankelijke statussen** is niet beschikbaar voor acties met als aanvankelijk actietype **Bericht maken**.

| Veld               | Beschrijving |
|---------------------|-------------|
| Status berichtitem | Selecteer de berichtitemstatus waarvoor de geselecteerde berichtverwerkingsactie moet worden beoordeeld. |
| Omschrijving         | Een omschrijving van de geselecteerde berichtitemstatus. |

#### <a name="result-statuses-fasttab"></a>Het sneltabblad Resulterende statussen

| Veld               | Omschrijving |
|---------------------|-------------|
| Berichtstatus      | Selecteer de berichtstatussen waarvoor de geselecteerde berichtverwerkingsactie moet worden beoordeeld. Dit veld is alleen beschikbaar voor berichtverwerkingsacties die worden beoordeeld op het berichtniveau. Het is bijvoorbeeld beschikbaar voor acties van het type **Export van elektronische rapportage** en **Import van elektronische rapportage**, maar is niet beschikbaar voor acties van het type **Verwerking door gebruiker** en **Uitvoeringsniveau berichtitem**. |
| Omschrijving         | Een omschrijving van de geselecteerde berichtstatus. |
| Antwoordtype       | Het antwoordtype van de geselecteerde berichtstatus. |
| Status berichtitem | Selecteer de resulterende statussen die beschikbaar moeten zijn nadat de geselecteerde berichtverwerkingsactie is beoordeeld. Dit veld is alleen beschikbaar voor berichtverwerkingsacties die worden beoordeeld op het berichtitemniveau. Het is bijvoorbeeld niet beschikbaar voor acties van het type **Verwerking door gebruiker** en **Uitvoeringsniveau berichtitem**. Voor berichtverwerkingsacties die worden beoordeeld op berichtniveau wordt in dit veld de berichtitemstatus weergegeven die is ingesteld voor de geselecteerde berichtstatus. |

De volgende tabel bevat de resultaatstatussen die moeten worden ingesteld voor verschillende actietypen en antwoordtypen.

| Actietype/antwoordtype elektronisch bericht | Uitgevoerd | Bedrijfsfout | Technische fout | Door gebruiker gedefinieerd | Annuleren |
|----------------------------------------------|-----------------------|----------------|-----------------|--------------|--------|
| Bericht maken                               | X                     |                |                 |              |        |
| Export van elektronische rapportage                  | X                     |                |                 |              |        |
| Import van elektronische rapportage                  |                       |                |                 |              |        |
| Webservice                                  | X                     |                | X               |              |        |
| Verwerking door gebruiker                              |                       |                |                 |              |        |
| Uitvoeringsniveau bericht                      |                       |                |                 |              |        |
| Records invullen                             |                       |                |                 |              |        |
| Uitvoeringsniveau berichtitem                 |                       |                |                 |              |        |
| Aanvraagverificatie                         | X                     | X              | X               |              |        |
| Bericht over export van elektronische rapportage          | X                     |                |                 |              |        |
| Verwerking door gebruiker van berichtniveau                |                       |                |                 |              |        |

### <a name="electronic-message-processing"></a>Elektronisch bericht verwerken

De verwerking van elektronische berichten is een basisconcept van de functionaliteit Elektronische berichten. Hiermee worden acties verzameld die moeten worden beoordeeld voor het elektronische bericht. De acties kunnen worden gekoppeld via een beginstatus en resultaatstatus. Acties van het type **Verwerking door gebruiker** kunnen ook onafhankelijk worden gestart. Op de pagina **Elektronisch bericht verwerken** (**Belasting** \> **Instellingen** \> **Elektronische berichten** \> **Elektronisch bericht verwerken**) kunt u ook aanvullende velden selecteren die moeten worden ondersteund voor de verwerking op berichtniveau of op berichtitemniveau.

Op het sneltabblad **Actie** kunt u vooraf gedefinieerde acties toevoegen aan de verwerking. U kunt opgeven of een actie afzonderlijk moet worden uitgevoerd of kan worden gestart door de verwerking. Als u wilt opgeven dat een actie in de verwerking alleen door een gebruiker kan worden geïnitialiseerd, stelt u het veld **Afzonderlijk uitvoeren** in op **Ja** voor die actie. Stel het veld **Afzonderlijk uitvoeren** in op **Nee** als een actie moet worden gestart door de verwerking wanneer voor berichten of berichtitems met de status die is gedefinieerd als de beginstatus voor de actie. Acties van het type **Gebruikersactie** moeten altijd afzonderlijk worden uitgevoerd.

Soms moeten meerdere acties worden samengevoegd in een reeks, zelfs als de eerste actie zo is ingesteld dat deze afzonderlijk wordt uitgevoerd. Bijvoorbeeld: een gebruiker moet het genereren van rapporten initialiseren, maar onmiddellijk nadat het rapport is gegenereerd moet het worden verzonden naar een webservice en moet het antwoord van de webservice worden weergegeven in het systeem. In dit geval kunt u een onscheidbare reeks maken voor de acties die altijd samen moeten worden uitgevoerd. Selecteer op het sneltabblad **Actie** **Onscheidbare reeksen** boven het raster en maak een reeks. Selecteer vervolgens voor alle acties die samen moeten worden uitgevoerd, de reeks in het veld **Onscheidbare reeks**. In dit geval kan het veld **Afzonderlijk uitvoeren** worden ingesteld op **Ja** voor de eerste actie in de reeks, maar op **Nee** voor alle andere acties.

Op het sneltabblad **Aanvullende velden berichtitem** kunt u extra vooraf gedefinieerde velden toevoegen die betrekking hebben op berichtitems. U moet extra velden toevoegen voor elk type berichtitem waarop de velden betrekking hebben.

Op het sneltabblad **Aanvullende velden voor bericht** kunt u extra vooraf gedefinieerde velden toevoegen die betrekking hebben op berichten.

Op het sneltabblad **Beveiligingsrollen** kunt u de beveiligingsrollen instellen die vooraf zijn gedefinieerd in het systeem voor specifieke verwerking. Gebruikers met een specifieke rol zien alleen de verwerking die is gedefinieerd voor die rol.

Op het sneltabblad **Batch** kunt u de verwerking voor een batchregime instellen.

## <a name="work-with-the-electronic-messages-functionality"></a>Werken met de functionaliteit Elektronische berichten

Als u op berichtniveau werkt, is de pagina **Elektronische berichten** (**Belasting** \> **Query's en rapporten** \> **Elektronische berichten** \> **Elektronische berichten**) geschikter. Als u op het niveau van gegevensverzameling (berichtitem) werkt, is de pagina **Items elektronisch bericht** (**Belasting** \> **Query's en rapporten** \> **Elektronische berichten** \> **Items elektronisch bericht**) geschikter.

### <a name="electronic-messages"></a>Elektronische berichten

Op de pagina **Elektronische berichten** wordt de verwerking weergegeven die voor u beschikbaar is, op basis van uw rol. Beveiligingsrollen worden aan verwerking gekoppeld bij het instellen van die verwerking. Voor elke verwerking die beschikbaar is voor u, worden op de pagina elektronische berichten en gerelateerde gegevens weergegeven.

Op het sneltabblad **Berichten** worden elektronische berichten voor de geselecteerde verwerking weergegeven. Afhankelijk van de status van het geselecteerde bericht en de vooraf gedefinieerde verwerking kunt u bepaalde acties uitvoeren met de knoppen boven het raster:

- **Nieuw**: deze knop is gekoppeld aan acties van het type **Bericht maken**.
- **Verwijderen**: deze knop is beschikbaar als het selectievakje **Verwijderen toestaan** is ingeschakeld voor de huidige status van het geselecteerde bericht.
- **Gegevens verzamelen**: deze knop is gekoppeld aan acties van het type **Records invullen**.
- **Rapport genereren**: deze knop is gekoppeld aan acties van het type **Bericht over export van elektronische rapportage**.
- **Rapport verzenden**: deze knop is gekoppeld aan acties van het type **Webservice**.
- **Antwoord importeren**: deze knop is gekoppeld aan acties van het type **Import van elektronische rapportage**.
- **Status bijwerken**: deze knop is gekoppeld aan acties van het type **Verwerking door gebruiker van berichtniveau**.
- **Berichtitems**: open de pagina **Items elektronisch bericht**.

Het sneltabblad **Actielogboek** bevat informatie over alle acties die zijn uitgevoerd voor het geselecteerde bericht. Als een actie een fout heeft veroorzaakt, wordt informatie over de fout gekoppeld aan de gerelateerde regel in het raster. Om informatie te bekijken over de fout, selecteert u de regel in het raster en selecteert u vervolgens de knop **Bijlage**  (de paperclip) in de rechterbovenhoek op de pagina.

Het sneltabblad **Aanvullende velden voor bericht** bevat alle extra velden die zijn gedefinieerd voor berichten in de instellingen voor verwerking. Ook de waarden van deze extra velden worden weergegeven.

Het sneltabblad **Berichtartikelen** bevat alle berichtartikelen die zijn gerelateerd aan het geselecteerde bericht. Afhankelijk van de status van het geselecteerde berichtitem kunt u bepaalde acties uitvoeren met de knoppen boven het raster:

- **Verwijderen**: deze knop is beschikbaar als het selectievakje **Verwijderen toestaan** is ingeschakeld voor de huidige status van het geselecteerde berichtitem.
- **Status bijwerken**: deze knop is gekoppeld aan acties van het type **Verwerking door gebruiker**.
- **Oorspronkelijk document**: open een pagina die het oorspronkelijke document voor het geselecteerde berichtitem bevat.

Alle rapporten die al zijn gegenereerd en ontvangen voor een bericht, worden aan dat bericht gekoppeld. Om de bijlagen te bekijken die zijn gerelateerd aan een bericht, selecteert u het bericht en selecteert u vervolgens de knop **Bijlage**  (de paperclip) in de rechterbovenhoek van de pagina.

![De knop Bijlage](media/attachment-icon.png)

De pagina **Bijlagen** bevat alle bijlagen die zijn gerelateerd aan het geselecteerde bericht. Als u een bestand wilt weergeven, selecteert u dit in de lijst links en selecteert u vervolgens **Openen** in het actievenster.

![De knop Openen](media/open-button.png)

U kunt ook bijlagen bekijken die zijn gerelateerd aan een bepaalde actie die eerder is uitgevoerd voor een bericht. Op de pagina **Elektronische berichten** selecteert u het bericht op het sneltabblad **Berichten**, selecteert u de actie op het sneltabblad **Actielogboek** en selecteert u vervolgens de knop **Bijlage** in de rechterbovenhoek van de pagina.

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
<td>Het rekeningnummer van een klant of leverancier (of een andere veldwaarde, afhankelijk van het veld dat is gedefinieerd voor de actie Records invullen). Dit veld kan alleen automatisch worden ingevuld als een factuur wordt toegevoegd aan de tabel Berichtitems.</td>
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

Selecteer **Verwerking uitvoeren** in het actievenster om de verwerking voor berichtitems uit te voeren. Als u een bepaalde actie wilt uitvoeren in het dialoogvenster **Verwerking uitvoeren**, stelt u de optie **Actie kiezen** in op **Ja** en selecteert u een actie. Als u de gehele verwerking wilt uitvoeren, laat u de optie **Actie kiezen** ingesteld op **Nee**.

#### <a name="generate-report"></a>Rapport genereren

Selecteer **Rapport genereren** in het actievenster om een rapport te genereren. Deze knop is gekoppeld aan acties van het type **Bericht over export van elektronische rapportage**.

#### <a name="update-status"></a>Status bijwerken

Selecteer **Status bijwerken** in het actievenster om de status van een of meer berichtitems bij te werken. Gebruik in het dialoogvenster **Status bijwerken** het sneltabblad **Op te nemen records** om de berichtitems te selecteren die u wilt bijwerken. Zorg ervoor dat u de selectiecriteria correct definieert, omdat berichtitemstatussen worden bijgewerkt volgens deze criteria, de oorspronkelijke status van de geselecteerde actie en de door u opgegeven waarde voor **Nieuwe status**. Nadat een statusupdate is voltooid, wordt het lastig om te bepalen welke items zijn bijgewerkt. Daarom is het moeilijk om de statusupdate terug te draaien.

#### <a name="electronic-messages"></a>Elektronische berichten

Selecteer **Elektronische berichten** in het actievenster om een elektronisch bericht te bekijken dat is gerelateerd aan het geselecteerde berichtitem.

U kunt ook alle bestanden bekijken die gerelateerd zijn aan een specifiek berichtitem. Selecteer het veld **Bericht** voor het berichtitem of selecteer **Elektronische berichten** in het actievenster. Selecteer vervolgens op de pagina **Elektronisch bericht** het bericht waarvoor u bestanden wilt bekijken en selecteer vervolgens de knop **Bijlage** (de paperclip) in de rechterbovenhoek van de pagina.

![De knop Bijlage](media/attachment-icon.png)

De pagina **Bijlagen** bevat alle bijlagen die zijn gerelateerd aan het bericht. Als u een bestand wilt weergeven, selecteert u dit in de lijst links en selecteert u vervolgens **Openen** in het actievenster.

![De knop Openen](media/open-button.png)

#### <a name="original-document"></a>Oorspronkelijk document

Selecteer **Oorspronkelijk document** in het actievenster om het oorspronkelijke document voor het geselecteerde berichtitem te openen.

## <a name="example-set-up-and-run-processing-to-call-a-simple-er-exporting-format-to-generate-an-excel-report"></a>Voorbeeld: verwerking instellen en uitvoeren om een eenvoudige ER-exportindeling aan te roepen en een Excel-rapport te genereren

Nadat u uw ER-indeling hebt gemaakt, hebt toegewezen aan gegevensbronnen en hebt voltooid, kunt u deze uitvoeren met behulp van het werkgebied **Elektronische rapportage**. Er wordt een rapport gegenereerd en u kunt het lokaal opslaan.

Als u de volgende aspecten van het rapportageproces wilt beheren, moet u de verwerking van elektronische berichten instellen:

- Informatie vastleggen over wie het rapport heeft gegenereerd.
- Informatie vastleggen over wanneer het rapport is gegenereerd.
- De rapporten opslaan die zijn gegenereerd voor vorige perioden.

Deze sectie bevat een voorbeeld waarin wordt aangegeven hoe u elektronische berichten kunt instellen om een rapport te genereren dat is gebaseerd op een ER-exportindeling voor Excel. Als u dit voorbeeld wilt volgen, moet u al een ER-exportindeling voor Excel hebben gemaakt, hebben toegewezen aan gegevensbronnen en hebben voltooid. Bovendien moet er al een nummerreeks zijn ingesteld voor elektronische berichten.

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
    - Op het sneltabblad **Resultaatstatussen** voegt u een aparte regel toe voor elk van de twee berichtstatussen (**Voorbereid** en **Nieuw**). Stel voor beide regels het veld **Antwoordtype** in op **Uitgevoerd**.

#### <a name="electronic-message-processing"></a>Elektronisch bericht verwerken

In dit voorbeeld moeten de acties zo worden ingesteld dat ze afzonderlijk worden uitgevoerd. Er wordt vanuit gegaan dat de gebruiker elke actie initialiseert.

1. Ga naar **Belasting \> Instellingen \> Elektronische berichten \> Elektronisch bericht verwerken**.
2. Voeg een record voor uw verwerking en alle eerder gedefinieerde acties en een extra veld toe.
3. Optioneel: definieer op het sneltabblad **Beveiligingsrollen** beveiligingsrollen voor uw verwerking om toegang te beperken tot specifieke rapportage.
4. Ga naar **Belasting \> Query's en rapporten \> Elektronische berichten \> Elektronische berichten**.
5. Selecteer **Nieuw** om een bericht te maken. Vervolgens kunt u datums en een omschrijving toevoegen. U kunt ook de waarde van het extra veld bijwerken.

    ![Een elektronisch bericht maken](media/create-electronic-message.png)

Het raster op het sneltabblad **Actielogboek** wordt automatisch gevuld met alle acties die worden uitgevoerd op het bericht.

U kunt de status van het bericht nu verwijderen of bijwerken. Selecteren **Status bijwerken** om de berichtstatus bij te werken. Selecteer in het veld **Nieuwe status** **Voorbereid** en selecteer vervolgens **OK**.

![De berichtstatus bijwerken](media/update-status.png)

De berichtstatus wordt bijgewerkt naar **Voorbereid** en u kunt het rapport nu genereren door **Rapport genereren** te selecteren. Het rapport wordt gegenereerd en de berichtstatus en het actielogboek worden bijgewerkt. Als u het gegenereerde rapport wilt weergeven, selecteert u de knop **Bijlage** (de paperclip) in de rechterbovenhoek van de pagina.
