---
title: Overzicht elektronische rapportage (ER)
description: Dit artikel biedt een overzicht van het hulpmiddel voor elektronische rapportage. In dit onderwerp worden belangrijke concepten, ondersteunde scenario's en indelingen beschreven die deel uitmaken van de oplossing.
author: kfend
ms.date: 11/02/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58941,  ""intro-internal
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.form: ERWorkspace
ms.openlocfilehash: e94846dd565abb6de2c1f07532d285e28307e9a2
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269686"
---
# <a name="electronic-reporting-er-overview"></a>Overzicht van elektronische rapportage (ER)

[!include [banner](../includes/banner.md)]

In dit artikel wordt een overzicht gegeven van het hulpmiddel voor Elektronische rapportage (ER). Er staat informatie in over belangrijke concepten, de scenario's die door ER ondersteund worden en een lijst met indelingen die als onderdeel van de ER-oplossing ontworpen en uitgegeven zijn.

ER is een configureerbaar hulpmiddel waarmee u wettelijke elektronische rapportage en betalingen kunt maken en onderhouden. Het is gebaseerd op de volgende drie concepten:

- Configuratie in plaats van codering:

    - De configuratie kan worden uitgevoerd door een zakelijke gebruiker en vereist geen ontwikkelaar.
    - Het gegevensmodel wordt gedefinieerd in bedrijfstermen.
    - Er worden visuele editors gebruikt om de onderdelen van de ER-configuratie te maken.
    - De taal die voor gegevenstransformatie wordt gebruikt, lijkt op de taal die wordt gebruikt in Microsoft Excel.

- Eén configuratie voor meerdere Dynamics 365 Finance-versies:

    - Beheer één domeinspecifiek gegevensmodel dat in bedrijfstermen wordt gedefinieerd.
    - Isoleer details van toepassingsversies in versieafhankelijke gegevensmodeltoewijzingen.
    - Onderhoud de configuratie van één indeling voor meerdere versies van de huidige versie op basis van het gegevensmodel.

- Eenvoudige of automatische upgrade:

    - Versiebeheer van ER-configuraties wordt ondersteund.
    - De Microsoft Dynamics-bibliotheek met Lifecycle Services-activa (LCS) kan worden gebruikt als opslagplaats voor ER-configuraties, voor het uitwisselen van versies.
    - Lokalisaties die op oorspronkelijke ER-configuraties zijn gebaseerd, kunnen als onderliggende versies worden geïntroduceerd.
    - Een ER-configuratiestructuur is een hulpmiddel waarmee u afhankelijkheden van versies kunt controleren.
    - Verschillen in lokalisatie, of de deltaconfiguratie, worden geregistreerd om een automatische upgrade naar een nieuwe versie van de oorspronkelijke ER-configuratie mogelijk te maken.
    - Conflicten die tijdens de automatische upgrade van lokalisatieversies worden ontdekt, kunnen eenvoudig handmatig worden opgelost.

Met ER kunt u elektronische indelingsstructuren definiëren en vervolgens beschrijven hoe de structuren moeten worden gevuld op basis van gegevens en algoritmes. U kunt een formuletaal gebruiken die lijkt op de Excel-taal voor gegevenstransformatie. Om de toewijzing van de database aan indeling beter beheersbaar, herbruikbaar en onafhankelijk van indelingswijzigingen te maken, is een tussenliggend gegevensmodelconcept geïntroduceerd. Dankzij dit concept kunnen implementatiedetails worden verborgen voor de indelingstoewijzing en kan één gegevensmodel opnieuw worden gebruikt voor toewijzingen met meerdere indelingen.

U kunt ER gebruiken voor het configureren van indelingen voor inkomende en uitgaande elektronische documenten volgens de wettelijke voorschriften van verschillende landen en regio's. Met ER kunt u deze indelingen beheren tijdens hun levenscyclus. Zo kunt u bijvoorbeeld nieuwe voorschriften toepassen en bedrijfsdocumenten genereren in de vereiste indeling om langs elektronische gegevens te kunnen uitwisselen met overheidsinstanties, banken en andere partijen.

De ER-engine is gericht op zakelijke gebruikers in plaats van ontwikkelaars. Aangezien u indelingen configureert in plaats van code, verlopen de processen voor het maken en aanpassen van indelingen voor elektronische documenten sneller en gemakkelijker.

ER ondersteunt op dit moment de werkbladindelingen TEXT, XML, JSON, PDF, Microsoft Word, Microsoft Excel en OPENXML.

## <a name="capabilities"></a>Mogelijkheden

De ER-engine biedt de volgende mogelijkheden:

- De engine vertegenwoordigt een enkel gedeeld hulpmiddel voor elektronische rapportage in verschillende domeinen en vervangt meer dan 20 verschillende engines waarmee elektronische rapportage van welke aard dan ook voor Finance + Operations wordt uitgevoerd.
- De engine zorgt ervoor dat de indeling van een rapport losstaat van de huidige implementatie. Met andere woorden, de indeling is van toepassing op verschillende versies.
- De engine ondersteunt het maken van een aangepaste indeling die is gebaseerd op een oorspronkelijke indeling. Dit omvat ook mogelijkheden voor het automatisch uitvoeren van een upgrade van de aangepaste indeling wanneer er wijzigingen in de oorspronkelijke indeling optreden wegens vereisten voor localisatie of aanpassing.
- Het wordt het primaire standaardhulpmiddel voor ondersteuning van lokalisatiebehoeften bij elektronische rapportage, zowel voor Microsoft als voor Microsoft-partners;
- Het ondersteunt de mogelijkheid om indelingen te verspreiden onder partners en klanten via Microsoft Dynamics Lifecycle Services (LCS).

## <a name="key-concepts"></a>Belangrijke concepten

### <a name="main-data-flow"></a>Hoofdgegevensstroom

[![ER-hoofdgegevensstroom.](./media/ger-main-data-flow.jpg)](./media/ger-main-data-flow.jpg)

### <a name="component"></a>Component

Elektronische rapportage ondersteunt de volgende typen onderdelen:

- Gegevensmodel
- Modeltoewijzing
- Format
- Metagegevens

Zie [Onderdelen van elektronische rapportage](er-overview-components.md) voor meer informatie.

### <a name="configuration"></a><a name="Configuration"></a>Configuratie

De ER-configuratie is de wrapper voor een bepaald ER-onderdeel. Dat onderdeel kan een gegevensmodelonderdeel zijn of een indelingscomponent. Een configuratie kan verschillende versies van een ER-onderdeel bevatten. Elke configuratie is gemarkeerd als eigendom van een bepaalde configuratieprovider. De **Concept**-versie van een onderdeel van een configuratie kan worden bewerkt als de eigenaar van de configuratie als een actieve provider is geselecteerd in de ER-instellingen in de toepassing.

Elke modelconfiguratie bevat een gegevensmodelonderdeel. Een nieuwe indelingsconfiguratie kan worden afgeleid van een specifieke gegevensmodelconfiguratie. In de configuratiestructuur wordt de gemaakte indelingsconfiguratie gepresenteerd als een onderliggend element van de oorspronkelijke gegevensmodelconfiguratie.

De indelingsconfiguratie die wordt gemaakt bevat een indelingscomponent. Het gegevensmodelonderdeel van de oorspronkelijke modelconfiguratie wordt automatisch ingevoegd in de indelingscomponent van de onderliggende indelingsconfiguratie als een standaardgegevensbron.

Een ER-configuratie wordt gedeeld voor toepassingsbedrijven.

### <a name="provider"></a><a name="Provider"></a>Provider

De ER-provider is de partij-id die wordt gebruikt om de auteur (eigenaar) van elke ER-configuratie aan te duiden. Via ER kunt u de lijst met configuratieproviders beheren. Indelingsconfiguraties die worden vrijgegeven voor elektronische documenten als onderdeel van de Finance + Operations-oplossing zijn gemarkeerd als het eigendom van de configuratieprovider **Microsoft**.

Voor informatie over het registreren van een nieuwe ER-provider speelt u de taakbegeleiding **ER Een configuratieprovider maken en deze als actief markeren** af (onderdeel van het bedrijfsproces **7.5.4.3 Onderdelen van IT-services/oplossingen ophalen/ontwikkelen (10677)**).

### <a name="repository"></a><a name="Repository"></a>Opslagplaats

In een ER-opslagplaats worden ER-configuraties opgeslagen. De volgende typen ER-opslagplaatsen worden momenteel ondersteund: 

- Gedeelde LCS-bibliotheek
- LCS-project
- Bestandssysteem
- RCS
- Operations-resources
- Algemene opslagplaats

De opslagplaats **Gedeelde LCS-bibliotheek** biedt toegang tot de lijst met configuraties binnen de bibliotheek voor gedeelde activa in Lifecycle Services (LCS). Dit type ER-opslagplaats kan alleen worden geregistreerd voor de Microsoft-provider. Vanuit de LCS-bibliotheek voor gedeelde activa kunt u de meest recente versies van ER-configuraties importeren in het huidige exemplaar.

Een opslagplaats **LCS-project** biedt toegang tot de lijst met configuraties van een specifiek LCS-project (activabibliotheek voor LCS-project) dat is geselecteerd tijdens de registratie van de opslagplaats. Via ER kunt u gedeelde configuraties uploaden vanuit het huidige exemplaar naar een specifieke opslagplaats voor **LCS-projecten**. U kunt ook configuraties importeren vanuit een bepaalde opslagplaats voor **LCS-projecten** in het huidige exemplaar van uw apps voor financiën en bedrijfsactiviteiten.

Een opslagplaats **Bestandssysteem** biedt toegang tot de lijst met configuraties die zich als XML-bestanden in de opgegeven map bevinden van het lokale bestandssysteem op de computer waarop de AOS-service wordt gehost. De vereiste map is geselecteerd in de fase opslagplaatsregistratie. U kunt configuraties importeren vanuit een opslagplaats **Bestandssysteem** in het huidige exemplaar. 

Houd er rekening mee dat dit type opslagplaats toegankelijk is in de volgende omgevingen:

- Cloudomgevingen geïmplementeerd voor ontwikkelingsdoeleinden (met testmodellen van ingesloten suites)
- Lokaal geïmplementeerde omgevingen (on-premises)

Zie [ER-configuraties (Elektronische rapportage) importeren](./electronic-reporting-import-ger-configurations.md) voor meer informatie.

Een opslagplaats **RCS** biedt toegang tot de lijst met configuraties van een specifiek exemplaar van [Regulatory Configuration Service (RCS)](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration) dat is geselecteerd in de fase van registratie van de opslagplaats. Met ER kunt u voltooide of gedeelde configuraties vanuit het geselecteerde RCS-exemplaar importeren in het huidige exemplaar, zodat u ze kunt gebruiken voor elektronische rapportage.

Zie [ER-configuraties (Elektronische rapportage) importeren vanuit RCS](./rcs-download-configurations.md) voor meer informatie.

Een **algemene opslagplaats** biedt toegang tot de lijst met configuraties in de algemene opslagplaats in de [configuratieservice](/business-applications-release-notes/october18/dynamics365-finance-operations/regulatory-service-configuration). Dit type ER-opslagplaats kan alleen worden geregistreerd voor de Microsoft-provider. Vanuit de algemene opslagplaats kunt u de meest recente versies van ER-configuraties importeren in het huidige exemplaar.

Zie voor meer informatie [Configuraties voor Elektronische rapportage (ER) importeren uit de algemene opslagplaats van de configuratieservice](./er-download-configurations-global-repo.md).

De opslagplaats **Bronnen voor bedrijfsactiviteiten** biedt toegang tot de lijst met configuraties die Microsoft als ER-configuratieprovider aanvankelijk heeft vrijgegeven als onderdeel van de toepassingsoplossing. Deze configuraties kunnen worden geïmporteerd in het huidige exemplaar en worden gebruikt voor elektronische rapportage of voor het afspelen van voorbeeldtaakbegeleidingen. Zij kunnen ook worden gebruikt voor extra lokalisaties en aanpassingen. Houd er rekening mee dat de meest recente versies die door Microsoft ER-configuraties worden verschaft, moeten worden geïmporteerd vanuit de LCS-bibliotheek met behulp van de bijbehorende ER-opslagplaats.

Vereiste opslagplaatsen voor **LCS-project**, **Bestandssysteem** en **Regulatory Configuration Services (RCS)** kunnen afzonderlijk worden geregistreerd voor elke configuratieprovider van het huidige exemplaar. Elke opslagplaats kan aan een specifieke configuratieprovider zijn gekoppeld.

## <a name="supported-scenarios"></a>Ondersteunde scenario's

### <a name="building-a-data-model"></a>Een gegevensmodel maken

ER biedt een modelontwerper waarmee u een gegevensmodel kunt maken voor een bepaald bedrijfsdomein. Alle domeinspecifieke bedrijfsentiteiten, en de relaties hiertussen, kunnen als een hiërarchische structuur worden voorgesteld in een gegevensmodel. 

Speel de taakbegeleiding **ER Ontwerp domeinspecifiek gegevensmodel** af (onderdeel van het bedrijfsproces **7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)** om vertrouwd te raken met de details van dit scenario).

### <a name="translating-data-model-content"></a>Inhoud van gegevensmodel vertalen

De inhoud van een gegevensmodel (labels en omschrijvingen) kan worden vertaald in andere talen die in de toepassingen worden ondersteund. Mogelijk wilt u inhoud van een gegevensmodel vertalen om de volgende redenen:

- Tijdens het ontwerpproces om de inhoud begrijpelijker te maken voor ontwerpers van indelingen die een andere taal spreken en die het gegevensmodel gebruiken voor gegevenstoewijzing van indelingscomponenten.
- Maak tijdens de uitvoering de inhoud gebruiksvriendelijker door aanwijzingen en help te presenteren voor uitvoeringsparameters en tevens geconfigureerde validatieberichten (fouten en waarschuwingen) in de taal die de voorkeur heeft van de aangemelde gebruiker.

### <a name="configuring-data-model-mappings-for-outgoing-documents"></a>Gegevensmodeltoewijzingen voor uitgaande documenten configureren

ER biedt een ontwerper voor modeltoewijzing waarmee gebruikers gegevensmodellen kunnen toewijzen die zij hebben ontworpen voor specifieke toepassingsgegevensbronnen. Op basis van de toewijzing worden de gegevens geïmporteerd tijdens de uitvoering vanuit de geselecteerde gegevensbronnen in het gegevensmodel. Het gegevensmodel wordt vervolgens gebruikt als een abstracte gegevensbron van ER-indelingen die uitgaande elektronische documenten genereren. 

Speel de taakbegeleidingen **ER Definieer modeltoewijzing en selecteer gegevensbronnen** en **ER Wijs gegevensmodel toe aan geselecteerde gegevensbronnen** (onderdeel van het bedrijfsproces **7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)** af om uzelf vertrouwd te maken met de details van dit scenario).

### <a name="configuring-data-model-mappings-for-incoming-documents"></a>Gegevensmodeltoewijzingen voor inkomende documenten configureren

ER biedt een ontwerper voor modeltoewijzing waarmee gebruikers gegevensmodellen kunnen toewijzen die zij hebben ontworpen voor specifieke bestemmingen. Gegevensmodellen kunnen bijvoorbeeld worden toegewezen aan de bewerkbare gegevenscomponenten, zoals tabellen, gegevensentiteiten en weergaven. Op basis van de toewijzing worden de gegevens bijgewerkt tijdens de uitvoering met de gegevens uit het gegevensmodel. Als abstracte opslag van de ER-indeling wordt het gegevensmodel gevuld met gegevens die worden geïmporteerd vanuit een inkomend elektronisch document. 

### <a name="storing-a-designed-model-component-as-a-model-configuration"></a>Een ontworpen modelonderdeel opslaan als modelconfiguratie

ER kan een ontworpen gegevensmodel samen met gekoppelde gegevenstoewijzingen opslaan als een modelconfiguratie van het huidige exemplaar. In de volgende afbeelding wordt een voorbeeld getoond van dit type gegevensmodelconfiguratie (de configuratie van het betalingsmodel).

Speel de taakbegeleiding **ER Wijs gegevensmodel toe aan geselecteerde gegevensbronnen** af (onderdeel van het bedrijfsproces **7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)** om vertrouwd te raken met de details van dit scenario).

### <a name="building-a-format-that-uses-a-data-model-as-a-base"></a>Een indeling maken die een gegevensmodel als basis gebruikt

ER ondersteunt een indelingsontwerper die u kunt gebruiken om de indeling van een elektronisch document te maken voor een geselecteerd bedrijfsdomein door het modelonderdeel als basis te selecteren. Dezelfde ER-indelingsontwerper stelt u in staat een indeling als gegevensbron toe te wijzen die u maakt voor de gegevensmodeltoewijzing van een geselecteerd domein. 

Speel de taakbegeleiding **ER Ontwerp domeinspecifieke indeling** af (onderdeel van het bedrijfsproces **7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)** om vertrouwd te raken met de details van dit scenario).

### <a name="building-a-configuration-to-generate-electronic-documents-in-openxml-worksheet-format"></a>Een configuratie bouwen voor het genereren van elektronische documenten in OPENXML-werkbladindeling

De ER-indelingsontwerper kan worden gebruikt om een bepaald elektronisch document te maken in OPENXML-werkbladindeling. 

Speel de taakbegeleiding **ER Een configuratie maken voor het genereren van rapporten in OPENXML-indeling** af (onderdeel van het bedrijfsproces **7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)** om vertrouwd te raken met de details van dit scenario). Als onderdeel van de taakbegeleidingsstap voor het importeren van een sjabloon, gebruikt u het Excel-bestand [Sjabloon van betalingsrapport (SampleVendPaymWsReport.xlsx)](https://download.microsoft.com/download/3/f/0/3f0658b2-042c-43cf-a776-0f4c7f7cfe4e/SampleVendPaymWsReport.xlsx) als sjabloon.

### <a name="building-a-configuration-to-generate-electronic-documents-in-a-word-document-format"></a>Een configuratie bouwen voor het genereren van elektronische documenten in Word-documentindeling

De ER-indelingsontwerper kan worden gebruikt om een bepaald elektronisch document te maken in een Word-documentindeling. In de volgende afbeelding ziet u een voorbeeld van dit type indeling. Merk op dat deze indeling de bestaande ER-configuratie gebruikt, die oorspronkelijk is opgezet voor het genereren van de rapportuitvoer in OPENXML-indeling.

Speel de taakbegeleiding ER: een configuratie ontwerpen voor het genereren van rapporten in Microsoft Word-indeling af (onderdeel van het bedrijfsproces 7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)) om vertrouwd te raken met de details van dit scenario. Gebruik de volgende Word-bestanden als sjablonen voor de ER-indeling als onderdeel van de taakbegeleidingfase voor het importeren van een sjabloon:

- [Sjabloon van betalingsrapport (SampleVendPaymDocReport.docx)](https://download.microsoft.com/download/0/d/e/0de5a87c-95fc-4dfa-958f-285cb28b5b2b/SampleVendPaymDocReport.docx)
- [Gebonden sjabloon van betalingsrapport (SampleVendPaymDocReportBounded.docx)](https://download.microsoft.com/download/a/1/2/a126cb43-6281-4f7b-bde0-25e03ff9bc1e/SampleVendPaymDocReportBounded.docx)

### <a name="building-a-configuration-to-import-data-from-incoming-electronic-documents"></a>Een configuratie bouwen om gegevens te importeren vanuit inkomende elektronische documenten

De ER-indelingsontwerper kan worden gebruikt om een elektronisch document te beschrijven dat is gepland voor het importeren van gegevens in de indeling XML of tekst. De ontworpen indeling wordt gebruikt om inkomende documenten te parseren. De ER-indelingstoewijzingsontwerper kan worden gebruikt voor het definiëren van het binden van de elementen van de ontworpen indeling aan het gegevensmodel. 

Speel de taakbegeleiding ER: vereiste configuraties maken voor het importeren van gegevens uit een extern bestand af (onderdeel van het bedrijfsproces 7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)) om vertrouwd te raken met de details van dit scenario. Gebruik de volgende bestanden om deze begeleider af te spelen:

- [ER-gegevensmodelconfiguratie (1099model.xml)](https://download.microsoft.com/download/b/d/9/bd9e8373-d558-4ab8-aa9b-31981adc97ea/1099model.xml)
- [ER-indelingsconfiguratie (1099format.xml)](https://download.microsoft.com/download/e/8/7/e87154b0-b53f-431f-8e1e-0b7f7c9805a9/1099format.xml)
- [Voorbeeld van het inkomende document in XML-indeling (1099entries.xml)](https://download.microsoft.com/download/4/0/3/403a4958-df24-476a-b8b0-6843a9fa7f89/1099entries.xml)
- [Voorbeeld van de werkmap voor beheer van gegevens van inkomend document (1099entries.xlsx)](https://download.microsoft.com/download/6/0/0/6001abab-a331-48db-a939-41851fb0f5d0/1099entries.xlsx)

### <a name="storing-a-designed-format-component-in-a-format-configuration"></a>Een ontworpen indelingsonderdeel opslaan in een indelingsconfiguratie

ER kan een ontworpen indeling samen met de geconfigureerde gegevenstoewijzingen opslaan als een indelingsconfiguratie van het huidige exemplaar. In de voorgaande afbeelding wordt een voorbeeld gegeven van dit type indelingsconfiguratie (**BACS (UK)**, die is een onderliggend element vormt van de configuratie **Betalingsmodel**). Speel de taakbegeleiding **ER Ontwerp domeinspecifieke indeling** af (onderdeel van het bedrijfsproces **7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)** om vertrouwd te raken met de details van dit scenario).

### <a name="configuring-finance-to-start-to-use-a-created-format-internally"></a>Finance configureren om een gemaakte indeling intern te gaan gebruiken

De toepassing kan worden geconfigureerd voor gebruik van een gemaakte indeling voor het genereren van elektronische rapporten. De verwijzing naar de gemaakte indelingsconfiguratie moet worden gedefinieerd in de instellingen van een specifiek domein. Als u bijvoorbeeld een configuratie in ER-indeling wilt gaan gebruiken voor elektronische betalingen aan leveranciers in BACS-indeling, moet naar de indelingsconfiguratie worden verwezen in specifieke betalingsmethoden.

Speel de taakbegeleiding **ER Gebruik indeling om nieuwe elektronische documenten voor betalingen te genereren** af (onderdeel van het bedrijfsproces **7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)**) om bekend te raken met de details van dit scenario.

## <a name="handling-er-components"></a>ER-onderdelen verwerken

### <a name="publishing-an-er-component-in-lcs-to-offer-it-externally-localization"></a>Een ER-onderdeel publiceren in LCS om dit extern aan te bieden (lokalisatie)

De eigenaar van een onderdeel (model of indeling) dat is gemaakt, kan ER gebruiken voor het publiceren van de voltooide versie van het onderdeel naar LCS. Een opslagplaats van het type **LCS-project** voor de huidige ER-configuratieprovider is vereist. Als de status van de voltooide versie van een onderdeel wordt gewijzigd van **VOLTOOID** naar **GEDEELD**, wordt die versie gepubliceerd in LCS. Wanneer een onderdeel is gepubliceerd naar LCS, wordt de eigenaar van dit onderdeel een provider van de service om het onderdeel te ondersteunen. Als bijvoorbeeld de indelingsonderdeel is ontworpen om een wettelijk vereist elektronisch document te genereren (bijvoorbeeld in overeenstemming met een lokalisatiescenario), wordt ervan uitgegaan dat de indeling in overeenstemming met de wettelijke wijzigingen wordt gehouden en dat de provider nieuwe versies van het onderdeel zal uitgeven telkens wanneer moet worden voldaan aan nieuwe wettelijke vereisten. Speel de taakbegeleiding **ER Een configuratie naar Lifecycle Services uploaden** af (onderdeel van het bedrijfsproces **7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)** om vertrouwd te raken met de details van dit scenario).

### <a name="importing-an-er-component-from-lcs-to-use-it-internally"></a>Een ER-onderdeel importeren vanuit LCS om dit intern te maken

Met ER kunt u onderdelen vanuit LCS importeren naar het huidige exemplaar. Een opslagplaats van het type **LCS-project** is vereist. Wanneer een ER-onderdeel vanuit LCS naar het huidige exemplaar is geïmporteerd, wordt de eigenaar van het exemplaar een verbruiker van de service die door de eigenaar (auteur) van het geïmporteerde onderdeel wordt aangeboden. Als bijvoorbeeld een indelingsonderdeel is ontworpen om vanuit de toepassing een specifiek elektronisch document te genereren in een bepaalde land-/regiospecifieke indeling (lokalisatiescenario), wordt ervan uitgegaan dat de consument van de service in staat is updates te verkrijgen die worden uitgevoerd voor die indeling om ervoor te zorgen dat de indeling aan de wettelijke vereisten voldoet. Speel de taakbegeleiding **ER Een configuratie vanuit Lifecycle Services importeren** af (onderdeel van het bedrijfsproces **7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)** om vertrouwd te raken met de details van dit scenario).

### <a name="building-a-format-selecting-another-format-as-a-base-customization"></a>Een indeling maken door een andere indeling als basis te selecteren (aanpassing)

Met ER kunt u een nieuw (afgeleid) onderdeel maken op basis van de huidige versie van een onderdeel(basis) dat is geïmporteerd vanuit LCS. Stel bijvoorbeeld dat een gebruiker een nieuwe indeling wil afleiden om sommige speciale vereisten voor een elektronisch document te implementeren (zoals een extra veld of een uitgebreide omschrijving) ter ondersteuning van een aanpassingsscenario. Speel de taakbegeleiding **>ER Indeling upgraden door instelling van een nieuwe basis hiervan** af (onderdeel van bedrijfsproces **7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)**) om bekend te raken met de details van dit scenario.

### <a name="upgrading-a-format-selecting-a-new-version-of-base-format-rebase"></a>Een indeling upgraden door een nieuwe versie van de basisindeling (rebase) te selecteren.

Met ER kunt u automatisch wijzigingen in de meest recente versie van het basisondeel aanbrengen in de huidige conceptversie van het afgeleide onderdeel. Dit proces wordt *rebasing* genoemd. Zo kan bijvoorbeeld een nieuwe wijziging in de regelgeving die is geïntroduceerd in de laatste versie van de indeling die werd geïmporteerd vanuit LCS automatisch worden samengevoegd met de aangepaste versie van deze indeling van het elektronisch document. Alle wijzigingen die niet automatisch kunnen worden samengevoegd worden als conflicten beschouwd. Deze conflicten worden weergegeven voor handmatige oplossing in het ontwerpprogramma voor het desbetreffende onderdeel. Speel de taakbegeleiding **>ER Indeling upgraden door instelling van een nieuwe basis van de indeling** af (onderdeel van bedrijfsproces **7.5.5.3 Gewijzigd onderdeel voor IT-services en -oplossingen aanschaffen/ontwikkelen (10683)**) om bekend te raken met de details van dit scenario.

## <a name="list-of-er-configurations-that-have-been-released-in-finance"></a><a name="list-of-configurations"></a>Lijst met ER-configuraties die in Finance zijn vrijgegeven

De lijst met ER-configuraties voor Finance wordt continu bijgewerkt. Open de [Algemene opslagplaats](er-download-configurations-global-repo.md) om de lijst met ER-configuraties te bekijken die momenteel worden ondersteund. Op het sneltabblad **Details beëindiging** kunt u de informatie bekijken over configuraties die zijn beëindigd of die niet meer worden onderhouden. 

![Inhoud van de algemene opslagplaats op de pagina Opslagplaats van configuratie.](./media/er-overview-03.gif)

## <a name="additional-resources"></a>Aanvullende bronnen

- [Onderdelen van elektronische rapportage](er-overview-components.md)
- [Configuraties voor elektronische rapportage (ER) maken](electronic-reporting-configuration.md)
- [De levenscyclus van de configuratie van elektronische rapportage (ER) beheren](general-electronic-reporting-manage-configuration-lifecycle.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

