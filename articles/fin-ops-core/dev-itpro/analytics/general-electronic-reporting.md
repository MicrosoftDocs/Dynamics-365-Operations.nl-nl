---
title: Overzicht van elektronische rapportage (ER)
description: Dit onderwerp biedt een overzicht van het hulpmiddel voor Elektronische rapportage (ER). Er staat informatie in over belangrijke concepten, de scenario's die door ER ondersteund worden en een lijst met indelingen die als onderdeel van de ER-oplossing ontworpen en uitgegeven zijn.
author: NickSelin
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 11ed2101304c4e09744bbd10e94e9cd2a8db4da5
ms.sourcegitcommit: dd960cf07d8be791fd27c7bb72e6baa2d63ccd51
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/14/2019
ms.locfileid: "2578236"
---
# <a name="electronic-reporting-er-overview"></a>Overzicht van elektronische rapportage (ER)

[!include [banner](../includes/banner.md)]

Dit onderwerp biedt een overzicht van het hulpmiddel voor Elektronische rapportage (ER). Er staat informatie in over belangrijke concepten, de scenario's die door ER ondersteund worden en een lijst met indelingen die als onderdeel van de ER-oplossing ontworpen en uitgegeven zijn.

ER is een hulpprogramma dat u kunt gebruiken voor het configureren van indelingen voor inkomende en uitgaande elektronische documenten volgens de wettelijke voorschriften van verschillende landen/regio's. Met ER kunt u deze indelingen beheren tijdens hun levenscyclus. Zo kunt u bijvoorbeeld nieuwe voorschriften toepassen en bedrijfsdocumenten genereren in de vereiste indeling om langs elektronische gegevens te kunnen uitwisselen met overheidsinstanties, banken en andere partijen.

De ER-engine is gericht op zakelijke gebruikers in plaats van ontwikkelaars. Aangezien u indelingen configureert in plaats van code, verlopen de processen voor het maken en aanpassen van indelingen voor elektronische documenten sneller en gemakkelijker.

ER ondersteunt op dit moment de werkbladindelingen TEXT, Microsoft Word-document en OPENXML. Een extensie-interface biedt echter ondersteuning voor andere indelingen.

## <a name="capabilities"></a>Mogelijkheden
De ER-engine biedt de volgende mogelijkheden:

- De engine vertegenwoordigt een enkel gedeeld hulpmiddel voor elektronische rapportage in verschillende domeinen en vervangt meer dan 20 verschillende engines waarmee elektronische rapportage van welke aard dan ook voor Finance and Operations wordt uitgevoerd.
- De engine zorgt ervoor dat de indeling van een rapport losstaat van de huidige implementatie. Met andere woorden, de indeling is van toepassing op verschillende versies.
- De engine ondersteunt het maken van een aangepaste indeling die is gebaseerd op een oorspronkelijke indeling. Dit omvat ook mogelijkheden voor het automatisch uitvoeren van een upgrade van de aangepaste indeling wanneer er wijzigingen in de oorspronkelijke indeling optreden wegens vereisten voor localisatie of aanpassing.
- Het wordt het primaire standaardhulpmiddel voor ondersteuning van lokalisatiebehoeften bij elektronische rapportage, zowel voor Microsoft als voor Microsoft-partners;
- Het ondersteunt de mogelijkheid om indelingen te verspreiden onder partners en klanten via Microsoft Dynamics Lifecycle Services (LCS).

## <a name="key-concepts"></a>Belangrijke concepten
### <a name="components"></a>Componenten

ER ondersteunt twee typen onderdelen: **Gegevensmodel** en **Indeling**.

#### <a name="data-model-components"></a>Gegevensmodelonderdelen

Een gegevensmodelonderdeel is een abstracte representatie van een gegevensstructuur. Hiermee wordt een specifiek bedrijfsdomeingebied beschreven met voldoende detail om te voldoen aan de rapportagevereisten voor dat domein. Een gegevensmodelonderdeel bestaat uit de volgende elementen:

- Een gegevensmodel, als een set domeinspecifieke bedrijfsentiteiten en een hiërarchisch gestructureerde definitie van relaties tussen deze entiteiten
- Een modeltoewijzing die geselecteerde toepassingsgegevensbronnen koppelt aan individuele elementen van een gegevensmodel dat, tijdens de uitvoering, de gegevensstroom en regels voor het invullen van bedrijfsgegevens in een gegevensmodelonderdeel.

Een bedrijfsentiteit van een gegevensmodel wordt voorgesteld als een container (record). Bedrijfsonderdeeleigenschappen worden weergegeven als gegevensitems (velden). Elk gegevensitem heeft een unieke naam, label, omschrijving en waarde. De waarde van elk gegevensitem kan zodanig worden ontworpen dat deze wordt herkend als een tekenreeks, geheel getal, reëel getal, datum, opsomming, Boolean enzovoort. Bovendien kan het een andere record of lijst met records zijn.

Een enkel gegevensmodelonderdeel kan verschillende hiërarchieën met domeinspecifieke zakelijke entiteiten bevatten. Het kan ook modeltoewijzingen bevatten, die ondersteuning bieden voor een bepaalde rapportspecifiek gegevensstroom tijdens runtime. De hiërarchieën worden onderscheiden op basis van een enkele record die is geselecteerd als basis voor modeltoewijzing. Zo ondersteunt bijvoorbeeld het gegevensmodel van het gebied van het betalingsdomein mogelijk de volgende toewijzingen:

- Bedrijf \> Leverancier \> Betalingstransacties van het debiteurendomein
- Klant \> Bedrijf \> Betalingstransacties van het crediteurendomein

Houd er rekening mee dat zakelijke entiteiten zoals Bedrijf en Betalingstransacties slechts één keer worden ontworpen. Vervolgens worden zij opnieuw gebruikt door verschillende toewijzingen.

Een modeltoewijzing die ondersteuning biedt voor uitgaande elektronische documenten, heeft de volgende mogelijkheden:

- Er kunnen verschillende gegevenstypen worden gebruikt als gegevensbronnen voor een gegevensmodel. Er kan bijvoorbeeld gebruik worden gemaakt van tabellen, gegevensentiteiten, methoden of opsommingen.
- Er worden gebruikerinvoerparameters ondersteund die kunnen worden gedefinieerd als gegevensbronnen voor een gegevnsmodel wanneer bepaalde gegevens moeten worden opgegeven tijdens de uitvoering.
- Hij biedt ondersteuning voor de transformatie van gegevens in de vereiste groepen. Ook kunt u hiermee filteren, sorteren en gegevens optellen en logische berekende velden toevoegen die zijn ontwikkeld door middel van formules die vergelijkbaar zijn met Microsoft Excel-formules. Zie voor meer informatie het onderwerp [Formuleontwerper in elektronische rapportage](general-electronic-reporting-formula-designer.md).


Een modeltoewijzing die ondersteuning biedt voor inkomende elektronische documenten, heeft de volgende mogelijkheden:

- Deze kan verschillende bij te werken gegevenselementen als doel gebruiken. Deze gegevenselementen omvatten tabellen, gegevensentiteiten en weergaven. De gegevens kunnen worden bijgewerkt met behulp van de gegevens van inkomende elektronische documenten. In een enkele modeltoewijzing kunnen meerdere doelen worden gebruikt.
- Er worden gebruikerinvoerparameters ondersteund die kunnen worden gedefinieerd als gegevensbronnen voor een gegevnsmodel wanneer bepaalde gegevens moeten worden opgegeven tijdens de uitvoering.

Een gegevensmodelonderdeel is ontworpen voor elk zakelijk domein dat moet worden gebruikt als centrale gegevensbron voor rapportage, waarmee rapportage wordt geïsoleerd van de fysieke implementatie van gegevensbronnen voor Finance and Operations. Het vertegenwoordigt domeinspecifieke zakelijke concepten en functionaliteit in een indeling die het initiële ontwerp en later onderhoud van een rapportageformulier efficiënter maakt.

#### <a name="format-components-for-outgoing-electronic-documents"></a>Indelingscomponent voor uitgaande elektronische documenten

Een indelingsonderdeel is het schema van de rapportage-uitvoer die wordt gegenereerd tijdens de uitvoering. Een schema bestaat uit de volgende elementen:

- Een indeling die de structuur en de inhoud definieert van het uitgaande document voor elektronische rapportage dat wordt gegenereerd tijdens de uitvoering
- Gegevensbronnen, als een reeks van gebruikersinvoerparameters en een domeinspecifiek gegevensmodel dat een geselecteerde modeltoewijzing gebruikt
- Een indelingstoewijzing, als reeks van bindingen van indelingsgegevensbronnen die individuele elementen bevatten van een indeling die tijdens de uitvoering de gegevensstroom en de regels voor het genereren van de indelingsuitvoer specificeert.
- Een indelingsvalidatie, als een reeks configureerbare regels die de het genereren van het rapport tijdens runtime controleren, afhankelijk van de uitvoeringscontext. Zo kan er bijvoorbeeld een regel zijn die het genereren van betalingen van een leverancier onderbreekt en een uitzondering genereert, wanneer specifieke kenmerken van de geselecteerde leverancier ontbreken, zoals het bankrekeningnummer.

Een indelingsonderdeel ondersteunt de volgende functies:

- Het maken van rapportage-uitvoer als afzonderlijke bestanden in verschillende indelingen, zoals tekst, XML, Microsoft Word-document of werkblad.
- Het maken van meerdere afzonderlijke bestanden en het opnemen van die bestanden in zip-bestanden.

Een indelingscomponent biedt de mogelijkheid om specifieke bestanden toe te voegen die in de rapportage-uitvoer kunnen worden gebruikt:

- Excel-werkmappen die een werkblad bevatten dat kan worden gebruikt als sjabloon voor uitvoer in de OPENXML-werkbladindeling
- Word-documenten die een werkblad bevatten dat kan worden gebruikt als sjabloon voor uitvoer in de Microsoft Word-indeling
- Andere bestanden die als vooraf gedefinieerde bestanden kunnen worden opgenomen in de uitvoer van de indeling

In de volgende afbeelding ziet u hoe de gegevensstroomm voor deze indelingen verloopt.

[![Gegevensstroom voor uitgaande-indelingscomponenten](./media/ER-overview-02.png)](./media/ER-overview-02.png)

Voor het uitvoeren van een enkele ER-indelingsconfiguratie en het genereren van een uitgaand elektronisch document moet u de toewijzing van de indelingsconfiguratie bepalen.

#### <a name="format-components-for-incoming-electronic-documents"></a>Indelingscomponent voor inkomende elektronische documenten
Een indelingscomponent is het schema van het inkomende document dat tijdens de uitvoering wordt geïmporteerd. Een schema bestaat uit de volgende elementen:

- Een indeling die de structuur en de inhoud definieert van het inkomende elektronische document dat gegevens bevat die tijdens de uitvoering worden geïmporteerd. Een indelingscomponent wordt gebruikt om een inkomend document te parseren in verschillende indelingen, zoals tekst en XML.
- Een indelingstoewijzing die afzonderlijke elementen bindt aan elementen van een domeinspecifiek gegevensmodel. Tijdens de uitvoering specificeren de elementen in het gegevensmodel de gegevensstroom en de regels voor het importeren van gegevens uit een inkomend document en slaan daarna de gegevens op in een gegevensmodel.
- Een indelingsvalidatie, als een reeks configureerbare regels die de het importeren van gegevens tijdens runtime controleren, afhankelijk van de uitvoeringscontext. Zo kan er bijvoorbeeld een regel zijn die het de import van gegevens van een bankafschrift met leveranciersbetalingen onderbreekt en een uitzondering genereert, wanneer specifieke kenmerken van een leverancier ontbreken, zoals de leveranciers-id.

In de volgende afbeelding ziet u hoe de gegevensstroomm voor deze indelingen verloopt.

[![Gegevensstroom voor inkomende-indelingscomponenten](./media/ER-overview-03.png)](./media/ER-overview-03.png)

Als u een enkele ER-indelingsconfiguratie wilt uitvoeren om gegevens te importeren uit een inkomend elektronisch document, moet u de gewenste toewijzing van een indelingsconfiguratie bepalen en ook het integratiepunt van een modeltoewijzing. U kunt dezelfde modeltoewijzing en bestemmingen samen gebruiken met verschillende indelingen voor verschillende typen inkomende documenten.

#### <a name="component-versioning"></a>Componentversiebeheer

Versiebeheer wordt ondersteund voor ER-onderdelen. De volgende werkstroom voorziet in het beheer van wijzigingen in ER-onderdelen:

1. De versie die oorspronkelijk is gemaakt, wordt gemarkeerd als een **Concept**-versie. Deze versie kan worden bewerkt en is beschikbaar voor testruns.
2. De **Concept**-versie kan worden geconverteerd naar een **Voltooide** versie. Deze versie kan worden gebruikt in lokale rapportageprocessen.
3. De **Voltooide** versie kan worden geconverteerd naar een **Gedeelde** versie. Deze versie is gepubliceerd in LCS en kan worden gebruikt in algemene rapportageprocessen.
4. De **Gedeelde** versie kan worden geconverteerd naar een **Vervallen** versie. Deze versie kan vervolgens worden verwijderd.

Versies met de status **Voltooid** of **Gedeeld** zijn beschikbaar voor andere gegevensuitwisseling. Op onderdelen met een van deze statussen kunnen deze acties worden uitgevoerd:

- Het onderdeel kan worden geserialiseerd in XML-indeling en geëxporteerd als bestand in XML-indeling.
- Een component kan opnieuw worden geserialiseerd vanuit een XML-bestand en geïmporteerd de toepassing als een nieuwe versie van een ER-onderdeel.

#### <a name="component-date-effectivity"></a>Effectivity van de componentdatum

Versies van ER-onderdelen zijn datumeffectief. U kunt de datum **Geldig vanaf** definiëren voor een ER-onderdeel, om de datum op te geven waarop een onderdeel geldig wordt voor rapportageprocessen. De datum van toepassingssessie wordt gebruikt om te definiëren of een onderdeel geldig is voor uitvoering. Als meer dan één versie geldig is voor een specifieke datum, wordt de meest recente versie gebruikt voor rapportageprocessen.

#### <a name="component-access"></a>Componenttoegang

Toegang tot ER-indelingsonderdelen is afhankelijk van de instelling voor de ISO land-/regiocode. Als deze instelling leeg wordt gelaten voor een geselecteerde versie van een indelingsconfiguratie, kan een indelingsonderdeel tijdens de uitvoering worden geopend vanuit elk bedrijf. Wanneer deze instelling ISO-land/regiocodes bevat, is alleen een indelingscomponent beschikbaar van bedrijven met een primair adres dat is gedefinieerd voor een van de ISO-land-/regiocodes van een indelingsonderdeel.

Verschillende versies van een gegevensindelingsonderdeel kunnen verschillende instellingen hebben voor ISO-land-/regiocodes.

#### <a name="configuration"></a>Configuratie

De ER-configuratie is de wrapper voor een bepaald ER-onderdeel. Dat onderdeel kan een gegevensmodelonderdeel zijn of een indelingscomponent. Een configuratie kan verschillende versies van een ER-onderdeel bevatten. Elke configuratie is gemarkeerd als eigendom van een bepaalde configuratieprovider. De **Concept**-versie van een onderdeel van een configuratie kan worden bewerkt als de eigenaar van de configuratie als een actieve provider is geselecteerd in de ER-instellingen in de toepassing.

Elke modelconfiguratie bevat een gegevensmodelonderdeel. Een nieuwe indelingsconfiguratie kan worden afgeleid van een specifieke gegevensmodelconfiguratie. In de configuratiestructuur wordt de gemaakte indelingsconfiguratie gepresenteerd als een onderliggend element van de oorspronkelijke gegevensmodelconfiguratie.

De indelingsconfiguratie die wordt gemaakt bevat een indelingscomponent. Het gegevensmodelonderdeel van de oorspronkelijke modelconfiguratie wordt automatisch ingevoegd in de indelingscomponent van de onderliggende indelingsconfiguratie als een standaardgegevensbron.

Een ER-configuratie wordt gedeeld voor toepassingsbedrijven.

#### <a name="provider"></a>Provider

De ER-provider is de partij-id die wordt gebruikt om de auteur (eigenaar) van elke ER-configuratie aan te duiden. Via ER kunt u de lijst met configuratieproviders beheren. Indelingsconfiguraties die worden vrijgegeven voor elektronische documenten als onderdeel van de Finance and Operations-oplossing zijn gemarkeerd als het eigendom van de configuratieprovider **Microsoft**.

Voor informatie over het registreren van een nieuwe ER-provider speelt u de taakbegeleiding **ER Een configuratieprovider maken en deze als actief markeren** af (onderdeel van het bedrijfsproces **7.5.4.3 Onderdelen van IT-services/oplossingen ophalen/ontwikkelen (10677)**).

#### <a name="repository"></a>Opslagplaats

In een ER-opslagplaats worden ER-configuraties opgeslagen. De volgende typen ER-opslagplaatsen worden momenteel ondersteund: 

- Gedeelde LCS-bibliotheek
- LCS-project
- Bestandssysteem
- Regulatory Configuration Services (RCS)
- Bronnen voor bedrijfsactiviteiten


De opslagplaats **Gedeelde LCS-bibliotheek** biedt toegang tot de lijst met configuraties binnen de bibliotheek voor gedeelde activa in Lifecycle Services (LCS). Dit type ER-opslagplaats kan alleen worden geregistreerd voor de Microsoft-provider. Vanuit de LCS-bibliotheek voor gedeelde activa kunt u de meest recente versies van ER-configuraties importeren in het huidige exemplaar.

Een opslagplaats **LCS-project** biedt toegang tot de lijst met configuraties van een specifiek LCS-project (activabibliotheek voor LCS-project) dat is geselecteerd in de fase van registratie van de opslagplaats. Via ER kunt u gedeelde configuraties uploaden vanuit het huidige exemplaar naar een specifieke opslagplaats voor **LCS-projecten**. U kunt ook configuraties importeren vanuit een bepaalde opslagplaats voor **LCS-projecten** in het huidige exemplaar van Finance and Operations.

Een opslagplaats **Bestandssysteem** biedt toegang tot de lijst met configuraties die zich als XML-bestanden bevinden in de opgegeven map van het lokale bestandssysteem op de computer waarop de AOS-service wordt gehost. Vereiste map is geselecteerd in de fase van opslagplaatsregistratie. U kunt configuraties importeren vanuit een opslagplaats **Bestandssysteem** in het huidige exemplaar. 

Houd er rekening mee dat dit type opslagplaats toegankelijk is in de volgende omgevingen:

- Cloudomgevingen geïmplementeerd voor ontwikkelingsdoeleinden (met testmodellen van ingesloten suites)
- Lokaal geïmplementeerde omgevingen (on-premises)

Zie [ER-configuraties (Elektronische rapportage) importeren](./electronic-reporting-import-ger-configurations.md) voor meer informatie.

Een opslagplaats **RCS-exemplaar** biedt toegang tot de lijst met configuraties van een specifiek RCS-exemplaar dat is geselecteerd in de fase van registratie van de opslagplaats. Met ER kunt u voltooide of gedeelde configuraties vanuit het geselecteerde RCS-exemplaar importeren in het huidige exemplaar, zodat u ze kunt gebruiken voor elektronische rapportage.

Zie voor meer informatie [Configuraties voor Elektronische rapportage (ER) importeren uit Regulatory Configuration Services (RCS)](./rcs-download-configurations.md).

De opslagplaats **Bronnen voor bedrijfsactiviteiten** biedt toegang tot de lijst met configuraties die Microsoft als ER-configuratieprovider aanvankelijk heeft vrijgegeven als onderdeel van de toepassingsoplossing. Deze configuraties kunnen worden geïmporteerd in het huidige exemplaar en worden gebruikt voor elektronische rapportage of voor het afspelen van voorbeeldtaakbegeleidingen. Zij kunnen ook worden gebruikt voor extra lokalisaties en aanpassingen. Houd er rekening mee dat de meest recente versies die door Microsoft ER-configuraties worden verschaft, moeten worden geïmporteerd vanuit de LCS-bibliotheek met behulp van de opslagplaats ER-opslagplaats.

Vereiste opslagplaatsen voor **LCS-project**, **Bestandssysteem** en **Regulatory Configuration Services (RCS)** kunnen afzonderlijk worden geregistreerd voor elke configuratieprovider van het huidige exemplaar. Elke opslagplaats kan aan een specifieke configuratieprovider zijn gekoppeld.

## <a name="supported-scenarios"></a>Ondersteunde scenario's
### <a name="building-a-data-model"></a>Een gegevensmodel maken

ER biedt een modelontwerper waarmee u een gegevensmodel kunt maken voor een bepaald bedrijfsdomein. Alle domeinspecifieke bedrijfsentiteiten, en de relaties hiertussen, kunnen als een hiërarchische structuur worden voorgesteld in een gegevensmodel. 

Speel de taakbegeleiding **ER Ontwerp domeinspecifiek gegevensmodel** af (onderdeel van het bedrijfsproces **7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)** om vertrouwd te raken met de details van dit scenario.

### <a name="translating-data-model-content"></a>Inhoud van gegevensmodel vertalen

De inhoud van een gegevensmodel (labels en omschrijvingen) kan worden vertaald in andere talen die in de toepassingen worden ondersteund. Mogelijk wilt u inhoud van een gegevensmodel vertalen om de volgende redenen:

- Tijdens het ontwerpproces om de inhoud begrijpelijker te maken voor ontwerpers van indelingen die een andere taal spreken en die het gegevensmodel gebruiken voor gegevenstoewijzing van indelingscomponenten.
- Maak tijdens de uitvoering de inhoud gebruiksvriendelijker door aanwijzingen en help te presenteren voor uitvoeringsparameters en tevens geconfigureerde validatieberichten (fouten en waarschuwingen) in de taal die de voorkeur heeft van de aangemelde gebruiker.

### <a name="configuring-data-model-mappings-for-outgoing-documents"></a>Gegevensmodeltoewijzingen voor uitgaande documenten configureren

ER biedt een ontwerper voor modeltoewijzing waarmee gebruikers gegevensmodellen kunnen toewijzen die zij hebben ontworpen voor specifieke toepassingsgegevensbronnen. Op basis van de toewijzing worden de gegevens geïmporteerd tijdens de uitvoering vanuit de geselecteerde gegevensbronnen in het gegevensmodel. Het gegevensmodel wordt vervolgens gebruikt als een abstracte gegevensbron van ER-indelingen die uitgaande elektronische documenten genereren. 

Speel de taakbegeleidingen **ER Definieer modeltoewijzing en selecteer gegevensbronnen** en **ER Wijs gegevensmodel toe aan geselecteerde gegevensbronnen** (onderdeel van het bedrijfsproces **7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)** af om uzelf vertrouwd te maken met de details van dit scenario.

### <a name="configuring-data-model-mappings-for-incoming-documents"></a>Gegevensmodeltoewijzingen voor inkomende documenten configureren
ER biedt een ontwerper voor modeltoewijzing waarmee gebruikers gegevensmodellen kunnen toewijzen die zij hebben ontworpen voor specifieke bestemmingen. Gegevensmodellen kunnen bijvoorbeeld worden toegewezen aan de bewerkbare gegevenscomponenten, zoals tabellen, gegevensentiteiten en weergaven. Op basis van de toewijzing worden de gegevens bijgewerkt tijdens de uitvoering met de gegevens uit het gegevensmodel. Als abstracte opslag van de ER-indeling wordt het gegevensmodel gevuld met gegevens die worden geïmporteerd vanuit een inkomend elektronisch document. 

### <a name="storing-a-designed-model-component-as-a-model-configuration"></a>Een ontworpen modelonderdeel opslaan als modelconfiguratie

ER kan een ontworpen gegevensmodel samen met gekoppelde gegevenstoewijzingen opslaan als een modelconfiguratie van het huidige exemplaar. In de volgende afbeelding wordt een voorbeeld getoond van dit type gegevensmodelconfiguratie (de configuratie van het betalingsmodel).

Speel de taakbegeleiding **ER Wijs gegevensmodel toe aan geselecteerde gegevensbronnen** af (onderdeel van het bedrijfsproces **7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)** om vertrouwd te raken met de details van dit scenario.

### <a name="building-a-format-that-uses-a-data-model-as-a-base"></a>Een indeling maken die een gegevensmodel als basis gebruikt

ER ondersteunt een indelingsontwerper die u kunt gebruiken om de indeling van een elektronisch document te maken voor een geselecteerd bedrijfsdomein door het modelonderdeel als basis te selecteren. Dezelfde ER-indelingsontwerper stelt u in staat een indeling als gegevensbron toe te wijzen die u maakt voor de gegevensmodeltoewijzing van een geselecteerd domein. 

Speel de taakbegeleiding **ER Ontwerp domeinspecifieke indeling** af (onderdeel van het bedrijfsproces **7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)** om vertrouwd te raken met de details van dit scenario.

### <a name="building-a-configuration-to-generate-electronic-documents-in-openxml-worksheet-format"></a>Een configuratie bouwen voor het genereren van elektronische documenten in OPENXML-werkbladindeling

De ER-indelingsontwerper kan worden gebruikt om een bepaald elektronisch document te maken in OPENXML-werkbladindeling. 

Speel de taakbegeleiding **ER Een configuratie maken voor het genereren van rapporten in OPENXML-indeling** af (onderdeel van het bedrijfsproces **7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)** om vertrouwd te raken met de details van dit scenario. Als onderdeel van de taakbegeleidingsstap voor het importeren van een sjabloon, gebruikt u het Excel-bestand [Sjabloon van betalingsrapport (SampleVendPaymWsReport.xlsx)](https://go.microsoft.com/fwlink/?linkid=845202) als sjabloon.

### <a name="building-a-configuration-to-generate-electronic-documents-in-a-word-document-format"></a>Een configuratie bouwen voor het genereren van elektronische documenten in Word-documentindeling
De ER-indelingsontwerper kan worden gebruikt om een bepaald elektronisch document te maken in een Word-documentindeling. In de volgende afbeelding ziet u een voorbeeld van dit type indeling. Merk op dat deze indeling de bestaande ER-configuratie gebruikt, die oorspronkelijk is opgezet voor het genereren van de rapportuitvoer in OPENXML-indeling.

Speel de taakbegeleiding ER: een configuratie ontwerpen voor het genereren van rapporten in Microsoft Word-indeling af (onderdeel van het bedrijfsproces 7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)) om vertrouwd te raken met de details van dit scenario. Gebruik de volgende Word-bestanden als sjablonen voor de ER-indeling als onderdeel van de taakbegeleidingfase voor het importeren van een sjabloon:

- [Sjabloon van betalingsrapport (SampleVendPaymDocReport.docx)](https://go.microsoft.com/fwlink/?linkid=845202)
- [Gebonden sjabloon van betalingsrapport (SampleVendPaymDocReportBounded.docx)](https://go.microsoft.com/fwlink/?linkid=845202)

### <a name="building-a-configuration-to-import-data-from-incoming-electronic-documents"></a>Een configuratie bouwen om gegevens te importeren vanuit inkomende elektronische documenten
De ER-indelingsontwerper kan worden gebruikt om een elektronisch document te beschrijven dat is gepland voor het importeren van gegevens in de indeling XML of tekst. De ontworpen indeling wordt gebruikt om inkomende documenten te parseren. De ER-indelingstoewijzingsontwerper kan worden gebruikt voor het definiëren van het binden van de elementen van de ontworpen indeling aan het gegevensmodel. 

Speel de taakbegeleiding ER: vereiste configuraties maken voor het importeren van gegevens uit een extern bestand af (onderdeel van het bedrijfsproces 7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)) om vertrouwd te raken met de details van dit scenario. Gebruik de volgende bestanden om deze begeleider af te spelen:

- [ER-gegevensmodelconfiguratie (1099model.xml)](https://go.microsoft.com/fwlink/?linkid=845202)
- [ER-indelingsconfiguratie (1099format.xml)](https://go.microsoft.com/fwlink/?linkid=845202)
- [Voorbeeld van het inkomende document in XML-indeling (1099entries.xml)](https://go.microsoft.com/fwlink/?linkid=845202)
- [Voorbeeld van de werkmap voor beheer van gegevens van inkomend document (1099entries.xlsx)](https://go.microsoft.com/fwlink/?linkid=845202)

### <a name="storing-a-designed-format-component-in-a-format-configuration"></a>Een ontworpen indelingsonderdeel opslaan in een indelingsconfiguratie

ER kan een ontworpen indeling samen met de geconfigureerde gegevenstoewijzingen opslaan als een indelingsconfiguratie van het huidige exemplaar. In de voorgaande afbeelding wordt een voorbeeld gegeven van dit type indelingsconfiguratie (**BACS (UK)**, die is een onderliggend element vormt van de configuratie **Betalingsmodel**). Speel de taakbegeleiding **ER Ontwerp domeinspecifieke indeling** af (onderdeel van het bedrijfsproces **7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)** om vertrouwd te raken met de details van dit scenario.

### <a name="configuring-finance-to-start-to-use-a-created-format-internally"></a>Finance configureren om een gemaakte indeling intern te gaan gebruiken

De toepassing kan worden geconfigureerd voor gebruik van een gemaakte indeling voor het genereren van elektronische rapporten. De verwijzing naar de gemaakte indelingsconfiguratie moet worden gedefinieerd in de instellingen van een specifiek domein. Als u bijvoorbeeld een configuratie in ER-indeling wilt gaan gebruiken voor elektronische betalingen aan leveranciers in BACS-indeling, moet naar de indelingsconfiguratie worden verwezen in specifieke betalingsmethoden.

Speel de taakbegeleiding **ER Gebruik indeling om nieuwe elektronische documenten voor betalingen te genereren** af (onderdeel van het bedrijfsproces **7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)**) om bekend te raken met de details van dit scenario.

## <a name="handling-er-components"></a>ER-onderdelen verwerken
### <a name="publishing-an-er-component-in-lcs-to-offer-it-externally-localization"></a>Een ER-onderdeel publiceren in LCS om dit extern aan te bieden (lokalisatie)

De eigenaar van een onderdeel (model of indeling) dat is gemaakt, kan ER gebruiken voor het publiceren van de voltooide versie van het onderdeel naar LCS. Een opslagplaats van het type **LCS-project** voor de huidige ER-configuratieprovider is vereist. Als de status van de voltooide versie van een onderdeel wordt gewijzigd van **VOLTOOID** naar **GEDEELD**, wordt die versie gepubliceerd in LCS. Wanneer een onderdeel is gepubliceerd naar LCS, wordt de eigenaar van dit onderdeel een provider van de service om het onderdeel te ondersteunen. Als bijvoorbeeld de indelingsonderdeel is ontworpen om een wettelijk vereist elektronisch document te genereren (bijvoorbeeld in overeenstemming met een lokalisatiescenario), wordt ervan uitgegaan dat de indeling in overeenstemming met de wettelijke wijzigingen wordt gehouden en dat de provider nieuwe versies van het onderdeel zal uitgeven telkens wanneer moet worden voldaan aan nieuwe wettelijke vereisten. Speel de taakbegeleiding **ER Een configuratie naar Lifecycle Services uploaden** af (onderdeel van het bedrijfsproces **7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)** om vertrouwd te raken met de details van dit scenario.

### <a name="importing-an-er-component-from-lcs-to-use-it-internally"></a>Een ER-onderdeel importeren vanuit LCS om dit intern te maken

Met ER kunt u onderdelen vanuit LCS importeren naar het huidige exemplaar. Een opslagplaats van het type **LCS-project** is vereist. Wanneer een ER-onderdeel vanuit LCS naar het huidige exemplaar is geïmporteerd, wordt de eigenaar van het exemplaar een verbruiker van de service die door de eigenaar (auteur) van het geïmporteerde onderdeel wordt aangeboden. Als bijvoorbeeld een indelingsonderdeel is ontworpen om vanuit de toepassing een specifiek elektronisch document te genereren in een bepaalde land-/regiospecifieke indeling (lokalisatiescenario), wordt ervan uitgegaan dat de consument van de service in staat is updates te verkrijgen die worden uitgevoerd voor die indeling om ervoor te zorgen dat de indeling aan de wettelijke vereisten voldoet. Speel de taakbegeleiding **ER Een configuratie vanuit Lifecycle Services importeren** af (onderdeel van het bedrijfsproces **7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)** om vertrouwd te raken met de details van dit scenario.

### <a name="building-a-format-selecting-another-format-as-a-base-customization"></a>Een indeling maken door een andere indeling als basis te selecteren (aanpassing)

Met ER kunt u een nieuw (afgeleid) onderdeel maken op basis van de huidige versie van een onderdeel(basis) dat is geïmporteerd vanuit LCS. Stel bijvoorbeeld dat een gebruiker een nieuwe indeling wil afleiden om sommige speciale vereisten voor een elektronisch document te implementeren (zoals een extra veld of een uitgebreide omschrijving) ter ondersteuning van een aanpassingsscenario. Speel de taakbegeleiding **>ER Indeling upgraden door instelling van een nieuwe basis hiervan** af (onderdeel van bedrijfsproces **7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)**) om bekend te raken met de details van dit scenario.

### <a name="upgrading-a-format-selecting-a-new-version-of-base-format-rebase"></a>Een indeling upgraden door een nieuwe versie van de basisindeling (rebase) te selecteren.

Met ER kunt u automatisch wijzigingen in de meest recente versie van het basisondeel aanbrengen in de huidige conceptversie van het afgeleide onderdeel. Dit proces wordt *rebasing* genoemd. Zo kan bijvoorbeeld een nieuwe wijziging in de regelgeving die is geïntroduceerd in de laatste versie van de indeling die werd geïmporteerd vanuit LCS automatisch worden samengevoegd met de aangepaste versie van deze indeling van het elektronisch document. Alle wijzigingen die niet automatisch kunnen worden samengevoegd worden als conflicten beschouwd. Deze conflicten worden weergegeven voor handmatige oplossing in het ontwerpprogramma voor het desbetreffende onderdeel. Speel de taakbegeleiding **>ER Indeling upgraden door instelling van een nieuwe basis van de indeling** af (onderdeel van bedrijfsproces **7.5.5.3 Gewijzigd onderdeel voor IT-services en -oplossingen aanschaffen/ontwikkelen (10683)**) om bekend te raken met de details van dit scenario.

## <a name="list-of-er-configurations-that-are-delivered-in-the-finance-application"></a>Lijst met ER-configuraties die worden geleverd in de Finance-toepassing

| Domeinspecifieke gegevensmodelconfiguraties: titel | Domein                | Configuratie van gegevensmodelafhankelijke indelingen: titel | Beschrijving                                                        |
|--------------------------------------------------|-----------------------|---------------------------------------------------|--------------------------------------------------------------------|
| Model van auditfile                                 | Financiële audit       |                                                   |                                                                    |
|                                                  |                       | Auditfile (NL)                                   | Auditfile-indeling voor Nederland                                  |
| BAS-model                                        | Belastingaangifte         |                                                   |                                                                    |
|                                                  |                       | BAS (AU)                                          | BAS-indeling voor Australië                                           |
| Schemamodel voor bouwsector               | Belastingaangifte         |                                                   |                                                                    |
|                                                  |                       | CIS maandretour (Verenigd Koninkrijk)                           | CIS maandelijkse retourindeling voor het Verenigd Koninkrijk                   |
| Model voor aanmaningsbrief                          | Elektronische facturering  |                                                   |                                                                    |
|                                                  |                       | OIOUBL Aanmaningsbrief (DK)                     | OIOUBL Indeling aanmaningsbrief voor Denemarken                        |
| 'Elektronisch grootboek boekhoudingsmodel (MX)          | Belastingaangifte         |                                                   |                                                                    |
|                                                  |                       | Hulpgrootboek XML (MX)                         | Rapportindeling voor transacties in hulpgrootboek per account voor Mexico |
|                                                  |                       | Rekeningschema XML (MX)                         | Indeling voor rapport van rekeningschema voor Mexico                          |
|                                                  |                       | Journalen XML (MX)                                 | Indeling voor rapport van journaaltransacties voor Mexico                      |
|                                                  |                       | Proefbalans XML (MX)                            | Indeling van proefbalansrapport voor Mexico                             |
| Elster-model                                     | Belastingaangifte         |                                                   |                                                                    |
|                                                  |                       | Elster (DE)                                       | Elster-indeling voor Duitsland                                          |
| Model van EU-verkooplijst                              | Handelsrapportage       |                                                   |                                                                    |
|                                                  |                       | EU-verkooplijst (DE)                                | TXT-indeling van EU-verkooplijst voor Duitsland                               |
|                                                  |                       | EU-verkooplijst (DK)                                | TXT-indeling van EU-verkooplijst voor Denemarken                               |
|                                                  |                       | EU-verkooplijst (FR)                                | XML-indeling van EU-verkooplijst voor Frankrijk                                |
|                                                  |                       | EU-verkooplijst (NL)                                | XML-indeling van EU-verkooplijst voor Nederland                           |
|                                                  |                       | TXT EU-verkooplijst (Verenigd Koninkrijk)                            | TXT-indeling van EU-verkooplijst voor het Verenigd Koninkrijk                    |
|                                                  |                       | XML EU-verkooplijst (Verenigd Koninkrijk)                            | XML-indeling van EU-verkooplijst voor het Verenigd Koninkrijk                    |
|                                                  |                       | Rapport van EU-verkooplijst in kolommen                   | Rapport van EU-verkooplijst in kolommen                                    |
|                                                  |                       | Rapport van EU-verkooplijst in rijen                      | Rapport van EU-verkooplijst in rijen                                       |
| FEC-boekhoudingsmodel (FR)                        | Belastingaangifte         |                                                   |                                                                    |
|                                                  |                       | FEC-boekhoudingsgegevens XML (FR)                      | Export in XML-indeling van FEC-boekhoudingsgegevens voor Frankrijk                   |
| Duits auditfile                                | Financiële audit       |                                                   |                                                                    |
|                                                  |                       | Uitvoer Duits auditfile                          | Uitvoer van auditfile voor Duitsland en Oostenrijk                          |
| Intrastat-model                                  | Handelsrapportage       |                                                   |                                                                    |
|                                                  |                       | Intrastat (DE)                                    | Intrastat-indeling voor Duitsland                                       |
|                                                  |                       | Intrastat (DK)                                    | Intrastat-indeling voor Denemarken                                       |
|                                                  |                       | Intrastat INTRACOM (FR)                           | Intrastat INTRACOM-indeling voor Frankrijk                               |
|                                                  |                       | Intrastat SAISUNIC (FR)                           | Intrastat SAISUNIC-indeling voor Frankrijk                               |
|                                                  |                       | Intrastat (NL)                                    | Intrastat-indeling voor Nederland                               |
|                                                  |                       | Intrastat (Verenigd Koninkrijk)                                    | Intrastat-indeling voor het Verenigd Koninkrijk                            |
|                                                  |                       | Intrastat-rapport                                  | Intrastat-controlerapport in Excel-indeling                                     |
| Klantfactuurmodel                           | Elektronische facturering  |                                                   |                                                                    |
|                                                  |                       | OIOUBL Projectcreditnota (DK)                   | OIOUBL Indeling van projectcreditnota voor Denemarken                      |
|                                                  |                       | OIOUBL Projectfactuur (DK)                       | OIOUBL Indeling van projectfactuur voor Denemarken                          |
|                                                  |                       | OIOUBL Verkoopcreditnota (DK)                     | OIOUBL Indeling van verkoopcreditnota voor Denemarken                        |
|                                                  |                       | OIOUBL Verkoopfactuur (DK)                         | OIOUBL Indeling van verkoopfactuur voor Denemarken                            |
| OB-aangiftemodel                             | Belastingaangifte         |                                                   |                                                                    |
|                                                  |                       | OB-aangifte (NL)                               | Indeling van OB-aangifte voor Nederland                          |
| Betalingsmodel                                    | Betalingen              |                                                   |                                                                    |
|                                                  |                       | Betalingsservice (DK)                             | Betalingsindeling van betalingsservice voor Denemarken                        |
|                                                  |                       | Bankremise voor wissel (FR)                  | Indeling van bankremise voor wissel voor Frankrijk                      |
|                                                  |                       | BTL91 (NL)                                        | BTL91 Indeling voor leveranciersbetaling voor Nederland                    |
|                                                  |                       | CFONB Prelevements (FR)                           | CFONB Indeling van betaling via automatische afschrijving voor Frankrijk                       |
|                                                  |                       | CFONB Virements (FR)                              | CFONB Indeling van betaling aan binnenlandse leverancier voor Frankrijk                    |
|                                                  |                       | Nordea Vendor (DK)                                | Indeling van leveranciersbetaling via Nordea Corporate Netbank voor Denemarken         |
|                                                  |                       | ANZ Direct Credit Service (AU)                    | Indeling voor ANZ Direct Credit Service voor Australië                 |
|                                                  |                       | CBA Direct Credit Service (AU)                    | Indeling voor CBA Direct Credit Service voor Australië                 |
|                                                  |                       | NAB Direct Credit Service (AU)                    | Indeling voor NAB Direct Credit Service voor Australië                 |
|                                                  |                       | STG Direct Credit Service (AU)                    | Indeling voor STG Direct Credit Service voor Australië                 |
|                                                  |                       | WBC Direct Entry System (AU)                      | Indeling voor WBC Direct Entry System voor Australië                   |
|                                                  |                       | DirectLink (NZ)                                   | Indeling voor DirectLink voor Nieuw-Zeeland                              |
|                                                  |                       | JBA Betalingsbestand (JP)                             | JBA Betalingsindeling voor Japan                                       |
|                                                  |                       | ISO20022 Kredietoverdracht                          | SEPA Indeling voor kredietoverdracht voor Europa                             |
|                                                  |                       | ISO20022 Kredietoverdracht (FR)                     | SEPA Indeling voor kredietoverdracht voor Frankrijk                             |
|                                                  |                       | ISO20022 Kredietoverdracht (DE)                     | SEPA Indeling voor kredietoverdracht voor Duitsland                            |
|                                                  |                       | ISO20022 Kredietoverdracht (NL)                     | SEPA Indeling voor kredietoverdracht voor Nederland                    |
|                                                  |                       | ISO20022 Automatische incasso                             | SEPA Indeling voor automatische incasso voor Europa                                |
|                                                  |                       | ISO20022 Automatische incasso (FR)                        | SEPA Indeling voor automatische incasso voor Frankrijk                                |
|                                                  |                       | ISO20022 Automatische incasso (DE)                        | SEPA Indeling voor automatische incasso voor Duitsland                               |
|                                                  |                       | ISO20022 Automatische incasso (NL)                        | SEPA Indeling voor automatische incasso voor Nederland                       |
|                                                  |                       | BACS (Verenigd Koninkrijk)                                         | BACS Indeling voor leveranciersbetaling voor het Verenigd Koninkrijk                  |
| Terugboeking                                   | Belastingaangifte         |                                                   |                                                                    |
|                                                  |                       | Verkooplijst terugboeken                         | Indeling voor terugboeking verkooplijst                                   |
| Nederlands XBRL-integratiemodel                     | XBRL-rapportering        |                                                   |                                                                    |
|                                                  |                       | Semansys XBRL (NL)                                | Semansys XBRL-exportindeling voor Nederland                    |
| GAF-model (MY)                                   | Financiële audit       |                                                   |                                                                    |
|                                                  |                       | GAF-bestand (MY)                                     | Indeling van GAF voor Maleisië                                         |
| Naar ouderdom gerangschikt rapport voor leveranciers (CN)                         | Analyse van leveranciersgegevens |                                                   |                                                                    |
|                                                  |                       | Indeling van naar ouderdom gerangschikt rapport voor leveranciers (CN)                   | Indeling van naar ouderdom gerangschikt rapport voor leveranciers voor China                               |
| Declaratiemodel voor leveranciersfacturen                 | Analyse van leveranciersgegevens |                                                   |                                                                    |
|                                                  |                       | Aangifte van leveranciersfacturen (IS)                   | Indeling voor aangifte van leveranciersfacturen voor IJsland                      |
|                                                  |                       | Rapport voor aangifte van leveranciersfacturen (IS)            | Rapport voor aangifte van leveranciersfacturen voor IJsland                      |

## <a name="additional-resources"></a>Aanvullende resources

- [Lokalisatievereisten – Een configuratie voor elektronische rapportage maken](electronic-reporting-configuration.md)
- [De levenscyclus van de configuratie van elektronische rapportage beheren](general-electronic-reporting-manage-configuration-lifecycle.md)
