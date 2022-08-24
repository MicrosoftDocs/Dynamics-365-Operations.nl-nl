---
title: Elektronische berichten instellen
description: Dit artikel bevat informatie over het instellen van de functionaliteit voor elektronische berichten (EM).
author: AdamTrukawka
ms.date: 11/18/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2021-06-23
ms.dyn365.ops.version: 8.0999999999999996
ms.openlocfilehash: 12beb1adbfa4e2f235c8a7c69e786d342c4a4f68
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9279297"
---
# <a name="set-up-electronic-messages"></a>Elektronische berichten instellen

[!include [banner](../includes/banner.md)]

De functionaliteit voor **Elektronische berichten** (EM) helpt u verschillende elektronische rapportageprocessen voor verschillende documenttypen te onderhouden. In sommige complexe scenario's met ondersteuning voor [landspecifieke rapportagefuncties](electronic-messaging.md#country-specific-regulatory-features-supported-by-the-em-functionality) wordt de EM-functionaliteit ingesteld om een combinatie van veel berichtstatussen, berichtitemstatussen, acties, extra velden en uitvoerbare klassen te hebben. Voor deze scenario's zijn pakketten met gegevensentiteiten beschikbaar voor import. Als u de pakketten met gegevensentiteiten wilt gebruiken, importeert u deze in een rechtspersoon met behulp van het hulpprogramma Gegevensbeheer. Zie [Gegevensbeheer](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md) voor meer informatie over het gebruik van het hulpprogramma Gegevensbeheer.

Als u een pakket met gegevensentiteiten niet importeert, kunt u de EM-functionaliteit handmatig instellen. In dat geval moet u de volgende onderdelen instellen:

- [Nummerreeksen](#sequences)
- [Typen berichtitems](#types)
- [Statussen berichtitem](#item)
- [Berichtstatussen](#statuses)
- [Aanvullende velden](#additional)
- [Uitvoerbare klasse-instellingen](#executable)
- [Acties voor invullen van record](#populate)
- [Records invullen vanuit meerdere bedrijven](#multiple-companies-populate)
- [Webtoepassingen](#applications)
- [Instellingen webservice](#settings)
- [Acties berichtverwerking](#actions)
- [Elektronisch bericht verwerken](#processing)

De volgende secties bevatten meer informatie over elk van deze onderdelen.

## <a name="number-sequences"></a><a id="sequences"></a>Nummerreeksen

Stel nummerreeksen in voor berichten en berichtitems. De nummerreeksen worden vervolgens gebruikt voor het automatisch nummeren van berichten en berichtitems. De nummers die worden toegewezen, worden gebruikt als unieke id's voor de berichten en berichtitems in het systeem. U kunt nummerreeksen voor elektronische berichten instellen door naar **Grootboek** \> **Grootboek instellen** \> **Grootboekparameters** te gaan.

## <a name="message-item-types"></a><a id="types"></a>Typen berichtitems

Met berichtitemtypen worden recordtypen aangeduid die worden gebruikt in elektronische berichten. U kunt berichtitemtypen instellen door naar **Belasting** \> **Instellingen** \> **Elektronische berichten** \> **Typen berichtitems** te gaan.

## <a name="message-item-statuses"></a><a id="item"></a>Statussen berichtitem

Met berichtitemstatussen worden de statussen aangeduid die van toepassing zijn op berichtitems in de verwerking die u instelt. U kunt statussen voor berichtitems instellen door naar **Belasting** \> **Instellingen** \> **Elektronische berichten** \> **Statussen berichtitem** te gaan.

Met de parameter **Verwijderen toestaan** van een berichtitemstatus wordt gedefinieerd of u berichtitems met deze status kunt verwijderen op de pagina **Elektronische berichten** of de pagina **Items elektronisch bericht**.

## <a name="message-statuses"></a><a id="statuses"></a>Berichtstatussen

Stel de berichtstatussen in die beschikbaar moeten zijn in de berichtverwerking. U kunt statussen voor berichten instellen door naar **Belasting** \> **Instellingen** \> **Elektronische berichten** \> **Berichtstatussen** te gaan.

In de volgende tabel worden de velden op de pagina **Berichtstatussen** beschreven.

| Veldnaam          | Beschrijving |
|---------------------|-------------|
| Berichtstatus      | Voer een unieke naam voor de berichtstatus in. Berichtstatussen worden gebruikt om de status van een elektronisch bericht op elk moment aan te geven. De naam die u invoert, wordt weergegeven op de pagina **Elektronische berichten** en in een logboek dat betrekking heeft op elektronische berichten. |
| Beschrijving         | Voer een omschrijving van de berichtstatus in. |
| Antwoordtype       | Selecteer het responstype voor de berichtstatus. Sommige acties in een verwerking kunnen meer dan één antwoordtype produceren. Zo kan bijvoorbeeld een actie van het type **Webservice** responsen produceren van het type **Uitgevoerd** of het type **Technische fout**, afhankelijk van het resultaat van de uitvoering ervan. Definieer in dit geval berichtstatussen voor beide responstypen. Zie de sectie [Actietypen voor berichtverwerking](#action-types) verderop in dit artikel voor meer informatie over actietypen en de eraan gerelateerde responstypen. |
| Status berichtitem | De status van een elektronisch bericht moet soms de status van gerelateerde berichtitems beïnvloeden. Selecteer een berichtitemstatus in dit veld om deze te koppelen aan de berichtstatus. |
| Verwijderen toestaan        | Schakel dit selectievakje in als gebruikers elektronische berichten met deze status op de pagina **Elektronische berichten** moeten kunnen verwijderen. |

## <a name="additional-fields"></a><a id="additional"></a>Aanvullende velden

Met de EM-functionaliteit kunt u records verzamelen uit transactietabellen in Microsoft Dynamics 365 Finance als berichtitems. Op deze manier kunt u de records voorbereiden voor rapportage en deze vervolgens rapporteren. Transactietabellen hebben soms echter onvoldoende gegevens om de records in te vullen op een manier die voldoet aan de rapportagevereisten. Om alle gegevens in te vullen die moeten worden gerapporteerd voor een record, kunt u extra velden instellen. Extra velden kunnen aan berichten en berichtitems worden gekoppeld. U kunt extra velden instellen door naar **Belasting** \> **Instellingen** \> **Elektronische berichten** \> **Aanvullende velden** te gaan.

In de volgende tabel worden de algemene velden op de pagina **Aanvullende velden** beschreven.

| Veld       | Beschrijving |
|-------------|-------------|
| Veldnaam  | Voer de naam in van een extra veld voor elektronische berichten of berichtitems die gerelateerd zijn aan het proces. Deze naam wordt weergegeven in de gebruikersinterface (UI) terwijl u met het proces werkt. De naam kan ook worden gebruikt in ER-configuraties (elektronische rapportage) die zijn gerelateerd aan het proces. |
| Beschrijving | Voer een omschrijving van het aanvullende veld in. |
| Bewerking door gebruiker   | Stel deze optie in op **Ja** als gebruikers de waarde van het extra veld in de gebruikersinterface moeten kunnen wijzigen. |
| Teller     | Stel deze optie in op **Ja** als het aanvullende veld een nummerreeks in een elektronisch bericht moet bevatten. De waarde van het extra veld wordt automatisch ingevuld tijdens het uitvoeren van een actie van het type **Export van elektronische rapportage**. |
| Verborgen      | Stel deze optie in op **Ja** als het extra veld moet worden verborgen in de gebruikersinterface op de pagina **Elektronische berichten** of de pagina **Elektronische berichtitems**. |

Op het sneltabblad **Waarden** kunt u vooraf waarden definieren die een extra veld kan hebben. Deze waarden kunnen gebruikers vervolgens selecteren. Ze hoeven daarom niet handmatig te worden ingevuld tijdens de verwerking. In de volgende tabel worden de velden beschreven.

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

## <a name="executable-class-settings"></a><a id="executable"></a>Uitvoerbare klasse-instellingen

Een uitvoerbare klasse is een X++-methode of -klasse die bij de verwerking van elektronische berichten kan worden aangeroepen in verband met een actie als er evaluatie nodig is voor het proces.

U kunt handmatig een uitvoerbare klasse instellen die tijdens de verwerking moet worden aangeroepen door naar **Belasting** \> **Instellingen** \> **Elektronische berichten** \> **Uitvoerbare klasse-instellingen** te gaan. Maak op de pagina **Uitvoerbare klasse-instellingen** een regel en stel de volgende velden in.

| Veld                 | Beschrijving |
|-----------------------|-------------|
| Uitvoerbare klasse      | Voer de naam in die wordt gebruikt tijdens het instellen van een berichtverwerkingsactie waarvoor deze klasse wordt aangeroepen. |
| Omschrijving           | Voer een omschrijving van de uitvoerbare klasse in. |
| Naam uitvoerbare klasse | Selecteer een uitvoerbare X++-klasse. |
| Uitvoeringsniveau       | Dit veld wordt automatisch ingesteld omdat de waarde vooraf is gedefinieerd voor de geselecteerde uitvoerbare klasse. Met dit veld beperkt u op welk niveau de gerelateerde evaluatie wordt uitgevoerd. |
| Klassenomschrijving     | Dit veld wordt automatisch ingesteld omdat de waarde vooraf is gedefinieerd voor de geselecteerde uitvoerbare klasse. |
| Actietype           | Dit veld is beschikbaar als de functie **\[EM\] Actietype voor uitvoerbare klasse** is ingeschakeld in het werkgebied **Functiebeheer**. Gebruik dit veld om het actietype voor de uitvoerbare klasse op te geven. Dit veld geeft nauwkeurigere controle over de volgende acties die beschikbaar zijn voor het elektronische bericht op de pagina **Elektronische berichten**. |

Sommige uitvoerbare klassen kunnen verplichte parameters hebben die moeten worden gedefinieerd voordat de uitvoerbare klasse voor de eerste keer wordt uitgevoerd. Als u deze parameters wilt definiëren, selecteert u **Parameters** in het actievenster. Stel in het dialoogvenster dat verschijnt de velden in en selecteer vervolgens **OK**. Het is belangrijk dat u **OK** selecteert. Anders worden de parameters niet opgeslagen in de database en wordt de uitvoerbare klasse niet correct opgeroepen.

## <a name="populate-records-actions"></a><a id="populate"></a>Acties voor invullen van record

U gebruikt acties voor het invullen van records om acties in te stellen waarmee records worden toegevoegd aan de tabel Berichtitems, zodat deze kunnen worden toegevoegd aan een elektronisch bericht. Als uw elektronische bericht bijvoorbeeld klantfacturen moet rapporteren, moet u een actie Records invullen instellen die is gekoppeld aan het veld **Gegevensbron** in de tabel Klantfacturenjournaal.

U kunt acties voor het invullen van records instellen door naar **Belasting** \> **Instellingen** \> **Elektronische berichten** \> **Acties voor invullen van record** te gaan. Maak een nieuwe record voor elke actie waarmee records moeten worden toegevoegd aan de tabel en stel de volgende velden in.

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
| Naam van hoofdtabel      | Selecteer de tabel die een gegevensbron moet worden. |
| Veld met documentnummer  | Selecteer het veld waaruit het documentnummer wordt gehaald in de geselecteerde hoofdtabel. De waarde van dit veld wordt gebruikt als de waarde van het veld **Documentnummer** voor het berichtitem. |
| Veld met documentdatum    | Selecteer het veld waaruit de documentdatum wordt gehaald in de geselecteerde hoofdtabel. De waarde van dit veld wordt gebruikt als de waarde van het veld **Datum berichtitem** voor het berichtitem. |
| Accountveld van document | Selecteer het veld waaruit het documentaccount wordt gehaald in de geselecteerde hoofdtabel. De waarde van dit veld wordt gebruikt als de waarde van het veld **Accountnummer** voor het berichtitem. |
| Bedrijf                | Dit veld is beschikbaar wanneer de functie **Query's voor meerdere bedrijven voor acties voor het invullen van records** is ingeschakeld in het werkgebied **Functiebeheer**. Gebruik deze functie om gegevensbronnen voor meerdere bedrijven in te stellen voor de acties voor het invullen van records. Gegevens kunnen worden opgehaald uit meerdere bedrijven. |
| Gebruikersquery             | <p>Als u een query instelt door **Query bewerken** boven het raster te selecteren en u de criteria opgeeft die moeten worden toegepast op de geselecteerde hoofdtabel waar gegevens van worden ingevuld, wordt dit selectievakje automatisch ingeschakeld. Anders worden alle records ingevuld via de geselecteerde hoofdtabelbron.</p><p>Wanneer de functie **Query's voor meerdere bedrijven voor acties voor het invullen van records** is ingeschakeld in het werkgebied **Functiebeheer** en records moeten worden verzameld vanuit verschillende bedrijven, voegt u een regel toe voor elke aanvullende rechtspersoon die in de rapportage moet worden opgenomen. Selecteer voor elke nieuwe regel **Query bewerken** en geef een gerelateerd criterium op dat specifiek is voor de rechtspersoon die is opgegeven in het veld **Bedrijf** op de regel. Wanneer u klaar bent, bevat het raster **Gegevensbroninstellingen** regels voor alle rechtspersonen die in de rapportage moeten worden opgenomen.</p> |

## <a name="populate-records-from-multiple-companies"></a><a id="multiple-companies-populate"></a>Records invullen vanuit meerdere bedrijven

Als uw bedrijf moet rapporteren over meerdere rechtspersonen in dezelfde Finance-database, stelt u de [acties voor het invullen van records](#populate) in voor alle rechtspersonen waarvan gegevens moeten worden opgenomen in de rapportage.

Volg deze stappen om deze mogelijkheid in te stellen in uw Finance-omgeving. 

1. Ga naar **Werkruimten** \> **Functiebeheer**.
2. Zoek en selecteer de functie **Query's voor meerdere bedrijven voor acties voor het invullen van records** in de lijst.
3. Selecteer **Nu inschakelen**. 

Volg deze stappen om de [acties voor het invullen van records](#populate) in te stellen voor meerdere bedrijven waaruit gegevens moeten worden opgenomen in de rapportage.

1. Ga naar **Belasting** \> **Instellingen** \> **Elektronische berichtens** \> **Acties voor invullen van record**.

    Wanneer de functie **Query's voor meerdere bedrijven voor acties voor het invullen van records** is ingeschakeld, bevat het raster **Instelling van gegevensbronnen** op de pagina **Actie voor invullen van record** een veld **Bedrijf**. Voor bestaande records die zijn gemaakt tijdens de algemene instelling van de functie [Acties voor invullen van record](#populate), bevat dit veld de id van de huidige rechtspersoon.

2. Voeg in het raster **Instelling van gegevensbronnen** een regel toe voor elke dochtermaatschappij die in de rapportage moet worden opgenomen en stel de volgende velden in.

    | Veldnaam             | Waarde |
    |------------------------|-------|
    | Name                   | Voer een tekst in om beter te begrijpen waar deze record vandaan komt. Voer bijvoorbeeld **Naam gegevensbron - Dochtermaatschappij 1** in. |
    | Type berichtitem      | Selecteer het berichtitemtype dat vereist is voor uw EM-verwerking. |
    | Rekeningtype           | Geef het accounttype op dat vereist is voor uw EM-verwerking. Als uw EM-verwerking geen specifieke accounttypen heeft, selecteert u **Alle**. |
    | Naam van hoofdtabel      | Geef de naam op van de hoofdtabel die vereist is voor uw EM-verwerking. |
    | Veld met documentnummer  | Geef het veld op dat het documentnummer bevat in records van uw EM-verwerking. |
    | Veld met documentdatum    | Geef het veld op dat de documentdatum bevat in records van uw EM-verwerking. |
    | Accountveld van document | Geef het veld op dat het documentaccount bevat in records van uw EM-verwerking. |
    | Bedrijf                | Selecteer de id van de dochtermaatschappij. |
    | Gebruikersquery             | Dit selectievakje wordt automatisch ingeschakeld wanneer u criteria definieert door **Query bewerken** te selecteren. |

3. Selecteer voor elke nieuwe regel **Query bewerken** en geef gerelateerde criteria op voor de rechtspersoon die is opgegeven in het veld **Bedrijf** op de regel.

## <a name="web-applications"></a><a id="applications"></a>Webtoepassingen

Gebruik webtoepassingsinstellingen om een webtoepassing in te stellen zodat deze Open Authorizaton (OAuth) 2.0 wordt ondersteund. OAuth is de open standard waarmee gebruikers 'beveiligde gedelegeerde toegang' tot de toepassing namens hen kunnen verlenen zonder dat ze hun toegangsreferenties hoeven te delen. U kunt ook het autorisatieproces doorlopen door een autorisatiecode en toegangstoken op te halen. U kunt webtoepassingsinstellingen instellen door naar **Belasting** \> **Instellingen** \> **Elektronische berichten** \> **Webtoepassingen** te gaan.

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
| Toegangstoken verloopt over  | De resterende tijd voordat het toegangstoken vervalt. Dit veld wordt automatisch bijgewerkt. | 
| Accepteren                       | Geef de eigenschap **Accepteren** van de webaanvraag op. Voer bijvoorbeeld **application/vnd.hmrc.1.0+json** in. |
| Inhoudstype                 | Geef het inhoudstype op. Voer bijvoorbeeld **application/json** in. |

Bovendien zijn de volgende knoppen beschikbaar in het actievenster van de pagina **Webtoepassingen** ter ondersteuning van het autorisatieproces:

- **Autorisatiecode ophalen**: autorisatie van de webtoepassing initialiseren. Deze functie gebruikt de ER-indeling die is opgegeven in het veld **Indelingstoewijzing voor autorisatie** om een autorisatieaanvraag te genereren.
- **Toegangstoken verkrijgen**: ophalen van een toegangstoken initialiseren.
- **Toegangstoken vernieuwen**: een toegangstoken vernieuwen. Deze functie gebruikt de ER-indeling die is opgegeven in het veld **Token modeltoewijzing importeren** om informatie over het ontvangen toegangstoken te importeren.

Wanneer een toegangstoken voor een webtoepassing in de database van het systeem in gecodeerde vorm is opgeslagen, kan het worden gebruikt voor aanvragen bij een webservice. Om beveiligingsredenen moet het token worden beperkt tot de beveiligingsrollen die zijn toegestaan om deze aanvragen af te handelen. Als iemand buiten de beveiligingsgroep probeert een aanvraag af te handelen, ontvangt hij of zij een foutbericht waarin wordt gemeld dat niet via de geselecteerde webtoepassing mag worden gewerkt. Als u de beveiligingsrollen wilt instellen die toegang tot het toegangstoken hebben, gebruikt u het sneltabblad **Beveiligingsrollen** op de pagina **Webtoepassingen**. Wanneer er geen beveiligingsrollen zijn gedefinieerd voor een webtoepassing, kan alleen een systeembeheerder via de webtoepassing werken.

Voor elke actie met de geselecteerde webtoepassing slaat het sneltabboek **Actielogboek** gegevens op over de gebruiker en de datum en tijd.

Voor sommige webservices moeten mogelijk verschillende kopteksten in de aanvragen worden opgenomen. De systeembeheerder kan extra kopteksten en de waarden ervan instellen op het sneltabblad **Bijkomende kopteksten** en deze vervolgens gebruiken tijdens het genereren van aanvragen.

## <a name="web-service-settings"></a><a id="settings"></a>Instellingen webservice

Gebruik webservice-instellingen om directe gegevensoverdracht naar een webservice in te stellen. U kunt webservice-instellingen opzetten door naar **Belasting** \> **Instellingen** \> **Elektronische berichten** \> **Instellingen webservice** te gaan.

In de volgende tabel worden de velden op de pagina **Webservice-instellingen** beschreven.

| Veld                          | Omschrijving |
|--------------------------------|-------------|
| Webservice                    | Geef een naam op voor de webservice. |
| Omschrijving                    | Geef een omschrijving van de webservice op. |
| Internetadres               | <p>Geef het internetadres van de webservice op. Als een webtoepassing is opgegeven voor de webservice en als het internetadres van de webservice identiek moet zijn aan het internetadres dat is gedefinieerd voor die webtoepassing, selecteert u **Basis-URL kopiëren**. De basis-URL van de webtoepassing wordt vervolgens naar dit veld gekopieerd.</p><p>**Waarschuwing:** services van derden of andere services die u hier configureert, vereisen geen certificering en voldoen mogelijk niet aan de privacynormen van Microsoft. U moet de privacydocumentatie van elke service controleren en met elke serviceprovider samenwerken om meer te weten te komen over het conformiteitsniveau dat de service biedt. Het is uw verantwoordelijkheid ervoor te zorgen dat deze services voldoen aan uw beveiligings-, privacy- en wettelijke normen. U bent zelf verantwoordelijk voor het gebruik van de services. Microsoft biedt geen uitdrukkelijke garantie, garanties of voorwaarden. Het wordt dringend aangeraden alleen services te gebruiken die beveiligde en geautoriseerde verbindingen bieden, zoals HTTPS.</p> |
| Getuigschrift                    | Selecteer een eerder ingesteld Azure Key Vault-certificaat. |
| Webtoepassing                | Selecteer een webtoepassing die eerder is ingesteld. |
| Het antwoordtype – XML        | Stel deze optie in op **Ja** als het responstype XML is. |
| Aanvraagmethode                 | Geeft aanvraagmethode op. HTTP definieert een set aanvraagmethoden waarmee wordt aangeven welke actie moet worden uitgevoerd voor een bepaalde bron. De aanvraagmethode kan **GET**, **POST** of een andere HTTP-methode zijn. |
| Kopteksten voor aanvraag                | Geef aanvraagkopteksten op. Een aanvraagkoptekst is een HTTP-koptekst die kan worden gebruikt in een HTTP-aanvraag. Deze informatie houdt geen verband met de inhoud van het bericht. |
| Accepteren                         | Geef de eigenschap voor accepteren van de webaanvraag op. |
| Versleuteling accepteren                | Geef de waarde voor het accepteren van versleuteling op. De HTTP-header van de Accept-Encoding-aanvraag adverteert de inhoudscodering die de client kan begrijpen. Deze inhoudscodering is meestal een algoritme voor compressie. |
| Inhoudstype                   | Geef het inhoudstype op. De HTTP-header van de entiteit Content-Type geeft het mediatype van de resource aan. |
| Geslaagde antwoordcode       | Geef de HTTP-statuscode op waarmee wordt aangegeven dat de aanvraag gelukt is. |
| Indelingstoewijzing van aanvraagkopteksten | Selecteer de ER-indeling die wordt gebruikt voor het genereren van webaanvraagkopteksten. |

## <a name="message-processing-actions"></a><a id="actions"></a>Acties berichtverwerking

U gebruikt berichtverwerkingsacties om acties voor uw processen te maken en de parameters in te stellen. U kunt verwerkingsacties voor berichten instellen door naar **Belasting** \> **Instellingen** \> **Elektronische berichten** \> **Acties berichtverwerking** te gaan.

In de volgende tabellen worden de velden op de pagina **Acties berichtverwerking** beschreven.

### <a name="general-fasttab"></a>Het sneltabblad Algemeen

| Veld                                     | Omschrijving |
|-------------------------------------------|-------------|
| Actietype                               | Selecteer het type actie. Zie de sectie [Actietypen voor berichtverwerking](#action-types) verderop in dit artikel voor informatie over de beschikbare opties. |
| Indelingstoewijzing                            | Selecteer de ER-indeling die voor de actie moet worden aangeroepen. Dit veld is alleen beschikbaar voor acties van het type **Export van elektronische rapportage**, **Import van elektronische rapportage** en **Bericht over export van elektronische rapportage**. |
| Indelingstoewijzing voor URL-pad               | Selecteer de ER-indeling die voor de actie moet worden aangeroepen. Deze indeling wordt gebruikt voor het samenstellen van het pad van het URL-adres dat wordt toegevoegd aan het basisinternetadres dat is opgegeven voor de geselecteerde webserver. Dit veld is alleen beschikbaar voor acties van het type **Webservice**. |
| Type berichtitem                         | Selecteer het recordtype waarvoor de actie moet worden beoordeeld. Dit veld is beschikbaar voor acties van het type **Uitvoeringsniveau berichtitem**, **Export van elektronische rapportage**, **Import van elektronische rapportage** en **Webservice** en andere typen. Als u dit veld leeg laat, worden alle gedefinieerde berichtitemtypen voor de berichtverwerking beoordeeld. |
| Uitvoerbare klasse                          | Selecteer een bestaande uitvoerbare klasse-instelling. Dit veld is alleen beschikbaar voor acties van het type **Uitvoeringsniveau** **berichtitem**. |
| Actie voor invullen van record                   | Selecteer een bestaande actie voor het invullen van records. Dit veld is alleen beschikbaar voor acties van het type **Records invullen**. |
| Webservice                               | Selecteer een bestaande webservice. Dit veld is alleen beschikbaar voor acties van het type **Webservice**. |
| Te verzenden bestandsnaam                         | Voer de naam in van de bijlage bij een elektronisch bericht die door deze actie moet worden verzonden. Als meerdere bijlagen dezelfde oorspronkelijke bestandsnaam hebben, wordt de nieuwste bijlage verzonden. Als er geen bijlage wordt gevonden met de opgegeven oorspronkelijke bestandsnaam, wordt de aanvraag zonder inhoud verzonden. Dit veld is alleen beschikbaar voor acties van het type **Webservice**. |
| Bestandsnaam                                 | Geef de naam op van het bestand dat het resultaat van de actie is. Dit bestand kan het antwoord zijn van de webserver of het rapport dat wordt gegenereerd. Dit veld is alleen beschikbaar voor acties van het type **Webservice** en **Bericht over export van elektronische rapportage**. |
| Bestanden toevoegen aan brondocumenten          | Schakel dit selectievakje in om gegenereerde bestanden te koppelen aan records in een hoofdtabel waarnaar wordt verwezen voor EM-items. Dit veld is alleen beschikbaar voor acties van het type **Export van elektronische rapportage** en **Webservice**. |
| Bestanden van archiefuitvoer koppelen aan items | Schakel dit selectievakje in om XML-bestanden te extraheren uit het uitvoerarchiefbestand en deze te koppelen aan de bijbehorende elektronische berichtitems. Dit veld is alleen beschikbaar voor acties van het type **Export van elektronische rapportage**. |
| Aantal weergegeven items per export        | Geef de limiet op voor het aantal berichtitems dat in één bestand (bericht) moet worden opgenomen. Dit veld is alleen beschikbaar voor acties van het type **Export van elektronische rapportage**. |
| ER-bron gebruiken                             | Schakel dit selectievakje in om ER-bronparameters te gebruiken voor importeren. Anders wordt de bijlage uit het elektronische bericht gebruikt. Dit veld is alleen beschikbaar voor acties van het type **Import van elektronische rapportage**. |
| Dialoogvenster weergeven                               | Stel deze optie in op **Ja** als een dialoogvenster moet worden weergegeven aan gebruikers voordat het rapport wordt gegenereerd. Dit veld is alleen beschikbaar voor acties van het type **Bericht over export van elektronische rapportage**. |

#### <a name="message-processing-action-types"></a><a id="action-types"></a>Actietypen voor berichtverwerking

De volgende opties zijn beschikbaar in het veld **Actietype**:

- **Bericht maken**: gebruik dit actietype om gebruikers handmatig berichten te laten maken op de pagina **Elektronische berichten**. Daarom kan geen beginstatus worden ingesteld voor een actie van dit type.
- **Records invullen**: dit actietype moet al zijn ingesteld. Koppel het aan een actie voor het invullen van records zodat de actie kan worden verwerkt. Hierbij wordt ervan uitgegaan dat dit actietype wordt gebruikt voor de eerste actie in de berichtverwerking (als er van tevoren geen elektronisch bericht is gemaakt) of als een actie waarbij berichtitems worden toegevoegd aan een eerder gemaakt bericht via het actietype **Bericht maken**. Daarom kan de resultaatstatus voor acties van dit type alleen voor berichtitems worden ingesteld. Een beginstatus kan alleen voor berichten worden ingesteld.
- **Uitvoeringsniveau bericht**: gebruik dit actietype voor het instellen van een uitvoerbare klasse die moet worden geëvalueerd op het berichtniveau.
- **Uitvoeringsniveau berichtitem**: gebruik dit actietype voor het instellen van een uitvoerbare klasse die moet worden geëvalueerd op het berichtitemniveau.
- **Export van elektronische rapportage**: gebruik dit actietype voor acties die een rapport moeten genereren dat is gebaseerd op een ER-exportconfiguratie op berichtitemniveau.
- **Bericht over export van elektronische rapportage**: gebruik dit actietype voor acties die een rapport moeten genereren dat is gebaseerd op een ER-exportconfiguratie op berichtitemniveau (bijvoorbeeld wanneer een bericht geen berichtitems bevat).
- **Import van elektronische rapportage**: gebruik dit actietype voor acties die een rapport moeten genereren dat is gebaseerd op een ER-importconfiguratie.
- **Verwerking door gebruiker van berichtniveau**: gebruik dit actietype voor acties waarbij wordt uitgegaan van enkele handmatige acties door de gebruiker op berichtniveau. De gebruiker kan bijvoorbeeld de status van berichten bijwerken.
- **Verwerking door gebruiker**: gebruik dit actietype voor acties waarbij wordt uitgegaan van enkele handmatige acties door de gebruiker op berichtitemniveau. De gebruiker kan bijvoorbeeld de status van berichtitems bijwerken.
- **Webservice**: gebruik dit actietype voor acties waarmee een gegenereerd rapport naar een webservice moet worden verzonden. Dit actietype wordt niet gebruikt voor de communicatie van Italiaanse inkoop- en verkoopfacturen. Voor dit actietype bevat de pagina **Acties berichtverwerking** een sneltabblad **Overige details** waar u een bevestigingstekst kunt opgeven. Deze bevestigingstekst wordt weergegeven aan gebruikers voordat aanvragen aan de geselecteerde webservice worden gericht.
- **Aanvraagverificatie**: gebruik dit actietype om verificatie van een server aan te vragen.

### <a name="initial-statuses-fasttab"></a>Het sneltabblad Aanvankelijke statussen

> [!NOTE]
> Het sneltabblad **Aanvankelijke statussen** is niet beschikbaar voor acties met als aanvankelijk actietype **Bericht maken**.

| Veld               | Beschrijving |
|---------------------|-------------|
| Status berichtitem | Selecteer de berichtitemstatus waarvoor de geselecteerde berichtverwerkingsactie moet worden beoordeeld. |
| Omschrijving         | Een omschrijving van de geselecteerde berichtitemstatus. |

### <a name="result-statuses-fasttab"></a>Het sneltabblad Resulterende statussen

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

## <a name="electronic-message-processing"></a><a id="processing"></a>Elektronisch bericht verwerken

De verwerking van elektronische berichten is een basisconcept van de EM-functionaliteit. Hiermee worden acties verzameld die moeten worden beoordeeld voor het elektronische bericht. De acties kunnen worden gekoppeld door gebruik te maken van een beginstatus en een resultaatstatus. Acties van het type **Verwerking door gebruiker** kunnen ook onafhankelijk worden gestart. Als u de verwerking van elektronische berichten wilt instellen, gaat u naar **Belasting** \> **Instellingen** \> **Elektronische berichten** \> **Elektronisch bericht verwerken**.

Op het sneltabblad **Actie** kunt u vooraf gedefinieerde acties toevoegen aan de verwerking. U kunt opgeven of een actie afzonderlijk moet worden uitgevoerd of kan worden gestart door de verwerking. Als u wilt opgeven dat een actie in de verwerking alleen door een gebruiker kan worden geïnitialiseerd, stelt u het veld **Afzonderlijk uitvoeren** in op **Ja** voor die actie. Stel het veld **Afzonderlijk uitvoeren** in op **Nee** als een actie moet worden gestart door de verwerking wanneer voor berichten of berichtitems met de status die is gedefinieerd als de beginstatus voor de actie. Acties van het type **Gebruikersactie** moeten altijd afzonderlijk worden uitgevoerd.

Soms moeten meerdere acties worden samengevoegd in een reeks, zelfs als de eerste actie is ingesteld op afzonderlijke uitvoering. Een gebruiker moet bijvoorbeeld het genereren van een rapport initialiseren. Nadat het rapport is gegenereerd, moet het naar een webservice worden verzonden en moet de respons van de webservice worden weergegeven in het systeem. In dit geval kunt u een onscheidbare reeks maken voor de acties die altijd samen moeten worden uitgevoerd. Selecteer op het sneltabblad **Actie** **Onscheidbare reeksen** boven het raster en maak een reeks. Selecteer vervolgens voor alle acties die samen in één reeks moeten worden uitgevoerd, de reeks in het veld **Onscheidbare reeks**. In dit voorbeeld kan het veld **Afzonderlijk uitvoeren** worden ingesteld op **Ja** voor de eerste actie in de reeks en op **Nee** voor alle andere acties.

Acties van de typen **Export van elektronische rapportage** en **Bericht over export van elektronische rapportage** voeren een ER-indeling met invoerparameters uit. Als bij de verwerking van elektronische berichten acties van een van deze typen worden gebruikt, moet u de waarden voor de invoerparameters opgeven voordat u een rapport kunt genereren. Op deze manier kan het systeem een batchregime gebruiken voor het genereren van het rapport. U kunt **Parameters** boven het raster selecteren om de parameters in te stellen voor het geselecteerde actietype (**Export van elektronische rapportage** of **Bericht over export van elektronische rapportage**). Schakel het selectievakje **Parameters gebruiken** in voor de actie die moet worden uitgevoerd met de opgegeven parameters in een batchregime.

Gebruik het sneltabblad **Aanvullende velden berichtitem** om extra vooraf gedefinieerde velden toe te voegen die betrekking hebben op berichtitems. U moet extra velden toevoegen voor elk type berichtitem waarop de velden betrekking hebben. U kunt een standaardwaarde opgeven die tijdens de verwerking aan het extra veld wordt toegewezen.

Gebruik het sneltabblad **Aanvullende velden voor bericht** om extra vooraf gedefinieerde velden toe te voegen die betrekking hebben op berichten. U kunt een standaardwaarde opgeven die tijdens de verwerking aan het extra veld wordt toegewezen.

Gebruik het sneltabblad **Beveiligingsrollen** om de beveiligingsrollen in te stellen die vooraf zijn gedefinieerd in het systeem voor specifieke verwerking. Gebruikers met een specifieke rol zien alleen de verwerking die is gedefinieerd voor die rol.

Gebruik het sneltabblad **Batch** om de verwerking voor een batchregime in te stellen. Het is raadzaam om een batchregime in te stellen voor uw verwerking direct op de pagina **Elektronische berichten** of **Elektronische berichtitems** wanneer u **Verwerking uitvoeren** selecteert in het actievenster om de verwerking te starten.
