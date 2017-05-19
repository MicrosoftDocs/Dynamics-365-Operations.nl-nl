---
title: Overzicht van elektronische rapportage
description: Dit artikel biedt een overzicht van het hulpmiddel voor Elektronische rapportage (ER). Er staat informatie in over belangrijke concepten, de scenario&quot;s die door ER ondersteund worden en een lijst met indelingen die als onderdeel van de ER-oplossing ontworpen en uitgegeven zijn.
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: abe9212372fb7429d68c1fb6b32ec1d15c20a6d7
ms.contentlocale: nl-nl
ms.lasthandoff: 04/25/2017


---

# <a name="electronic-reporting-overview"></a>Overzicht van elektronische rapportage

[!include[banner](../includes/banner.md)]


Dit artikel biedt een overzicht van het hulpmiddel voor Elektronische rapportage (ER). Er staat informatie in over belangrijke concepten, de scenario's die door ER ondersteund worden en een lijst met indelingen die als onderdeel van de ER-oplossing ontworpen en uitgegeven zijn.

Elektronische rapportage (ER) is een hulpprogramma dat u kunt gebruiken voor het configureren van indelingen voor elektronische documenten volgens de wettelijke voorschriften van verschillende landen/regio's. Met ER kunt u deze indelingen beheren tijdens hun levenscyclus. Zo kunt u bijvoorbeeld nieuwe voorschriften vaststellen en bedrijfsdocumenten genereren in de vereiste indeling om langs elektronische gegevens te kunnen uitwisselen met overheidsinstanties, banken en andere partijen. De ER-engine is gericht op zakelijke gebruikers in plaats van ontwikkelaars. Aangezien u indelingen configureert en geen code, verlopen de processen van het maken en aanpassen van indelingen voor elektronische documenten sneller en gemakkelijker. ER ondersteunt op dit moment de indelingen TEKST, XML en OPENXML-werkblad. Een extensie-interface biedt echter ondersteuning voor meer indelingen.

## <a name="capabilities"></a>Mogelijkheden
De ER-engine biedt de volgende mogelijkheden:

-   De engine vertegenwoordigt een enkel algemeen hulpmiddel voor elektronische rapportage in verschillende domeinen en vervangt meer dan 20 verschillende engines waarmee elektronische rapportage van welke aard dan ook voor Microsoft Dynamics 365 for Operations wordt uitgevoerd.
-   De engine zorgt ervoor dat de indeling van een rapport losstaat van de huidige implementatie van Dynamics 365 for Operations. (Met andere woorden, de indeling is van toepassing op verschillende versies van Dynamics 365 for Operations.)
-   De engine ondersteunt het maken van een aangepaste indeling die is gebaseerd op een oorspronkelijke indeling. Dit omvat mogelijkheden voor het automatisch uitvoeren van een upgrade van de aangepaste indeling wanneer er wijzigingen in de oorspronkelijke indeling optreden omdat localisatie-/aanpassingsvereisten worden geïntroduceerd.
-   Het wordt het primaire standaardhulpmiddel voor ondersteuning van lokalisatiebehoeften bij elektronische rapportage, zowel voor Microsoft als voor Microsoft-partners;
-   Het ondersteunt de mogelijkheid om indelingen te verspreiden onder partners en klanten via Microsoft Dynamics-Lifecycle Services (LCS).

## <a name="concepts"></a>Concepten
### <a name="components"></a>Onderdelen

ER ondersteunt twee typen onderdelen: **Gegevensmodel**en **Indeling**.

#### <a name="data-model-components"></a>Gegevensmodelonderdelen

Een gegevensmodelonderdeel is een abstracte weergave van een gegevensstructuur en wordt gebruikt voor het definiëren van een specifiek bedrijfsdomeingebied met voldoende details om aan de rapportagevereisten voor dat domein te voldoen. Een gegevensmodelonderdeel bestaat uit de volgende elementen:

-   Een gegevensmodel als een set domeinspecifieke bedrijfsentiteiten en een hiërarchisch gestructureerde definitie van relaties tussen deze entiteiten
-   Een modeltoewijzing die geselecteerde Dynamics 365 for Operations-gegevensbronnen koppelt aan individuele elementen van een gegevensmodel dat, tijdens de uitvoering, de gegevensstroom en regels voor het invullen van bedrijfsgegevens in een gegevensmodelonderdeel opgeeft.

Een bedrijfsentiteit van een gegevensmodel wordt voorgesteld als een container (record). Bedrijfsonderdeeleigenschappen worden weergegeven als gegevensitems (velden). Elk gegevensitem heeft een unieke naam, label, omschrijving en waarde. De waarde van elk gegevensitem kan zodanig worden ontworpen dat deze wordt herkend als een tekenreeks, geheel getal, reëel getal, datum, opsommingstype, Boolean enzovoort. Bovendien kan het een andere record of lijst met records zijn. Een enkel gegevensmodelonderdeel kan meerdere hiërarchieën bevatten van domeinspecifieke bedrijfsentiteiten en tevens modeltoewijzingen die een bepaalde rapportspecifieke gegevensstroom tijdens de uitvoering ondersteunen. De hiërarchieën worden onderscheiden op basis van een enkele record die is geselecteerd als basis voor modeltoewijzing. Zo ondersteunt bijvoorbeeld het gegevensmodel van het gebied van het betalingsdomein mogelijk de volgende toewijzingen:

-   Bedrijf -&gt; Leverancier -&gt; Betalingstransacties van het debiteurendomein
-   Klant -&gt; Bedrijf -&gt; Betalingstransacties van het crediteurendomein

Houd er rekening mee dat bedrijfsentiteiten (zoals Bedrijf en Betalingstransacties) eenmaal zijn ontworpen. Vervolgens worden zij opnieuw gebruikt door verschillende toewijzingen. Een modeltoewijzing biedt de volgende mogelijkheden:

-   Er kunnen verschillende gegevenstypen in Dynamics 365 for Operations worden gebruikt als gegevensbronnen voor een gegevensmodel. Er kan bijvoorbeeld gebruik worden gemaakt van tabellen, gegevensentiteiten, methoden of opsommingen.
-   Er worden gebruikerinvoerparameters ondersteund die kunnen worden gedefinieerd als gegevensbronnen voor een gegevnsmodel wanneer bepaalde gegevens moeten worden opgegeven tijdens de uitvoering.
-   Er wordt ondersteuning geboden voor de omzetting van Dynamics 365 for Operations-gegevens in vereiste groepen, filtering, sortering en optelling van gegevens en ook toevoeging van logisch berekende velden die zijn ontwikkeld met Microsoft Excel-achtige formules (zie [Formuleontwerper in Elektronische rapportage](general-electronic-reporting-formula-designer.md) voor meer informatie).

[![Excel-achtige formule-editor](./media/pic-formula-1024x615.png)](./media/pic-formula.png) Er wordt een gegevensmodelonderdeel ontworpen voor elk bedrijfsdomein dat dient te worden gebruikt als verenigde gegevensbron voor rapportage die rapportage isoleert van de fysieke implementatie van Dynamics 365 for Operations-gegevensbronnen en domeinspecifieke bedrijfsconcepten en functionaliteiten vertegenwoordigt in een vorm die het initiële ontwerp en verdere onderhoud van een rapportage-indeling efficiënter maakt.

#### <a name="format-components"></a>Indelingsonderdelen

Een indelingsonderdeel is het schema van de rapportage-uitvoer die wordt gegenereerd tijdens de uitvoering. Een schema bestaat uit de volgende elementen:

-   Een indeling die de structuur en de inhoud definieert van het document voor elektronische rapportage dat wordt gegenereerd tijdens de uitvoering
-   Gegevensbronnen als een reeks van gebruikersinvoerparameters en een domeinspecifiek gegevensmodel dat een geselecteerde modeltoewijzing gebruikt
-   Eeen indelingstoewijzing als reeks van bindingen van indelingsgegevensbronnen die individuele elementen bevatten van een indeling die, tijdens de uitvoering, de gegevensstroom en de regels voor het genereren van de indelingsuitvoer specificeert
-   Een indelingsvalidatie als een set van configureerbare regels die, tijdens de uitvoering, het genereren van rapporten regelt, afhankelijk van de uitvoeringscontext (bijvoorbeeld een regel die het genereren van betalingen van een leverancier stopt en een uitzondering genereert als specifieke kenmerken van de geselecteerde leverancier, zoals het bankrekeningnummer, ontbreken).

Een indelingsonderdeel ondersteunt de volgende functies:

-   Het maken van rapportage-uitvoer als afzonderlijke bestanden in verschillende indelingen: tekst, XML of werkblad
-   Het maken van meerdere aparte bestanden en ook het opnemen van die bestanden in zip-bestanden

Een indelingsonderdeel biedt de mogelijkheid om specifieke bestanden toe te voegen die in de rapportage-uitvoer kunnen worden gebruikt:

-   Excel-werkmappen die een werkblad bevatten dat kan worden gebruikt als sjabloon voor uitvoer in de OPENXML-werkbladindeling
-   Andere bestanden die als vooraf gedefinieerde bestanden kunnen worden opgenomen in de uitvoer van de indeling

#### <a name="component-versioning"></a>Componentversiebeheer

Versiebeheer wordt ondersteund voor ER-onderdelen. De volgende werkstroom wordt opgegeven voor het beheren van wijzigingen in ER-onderdelen:

-   De versie die oorspronkelijk is gemaakt, wordt gemarkeerd als een **CONCEPT**-versie. Deze versie kan worden bewerkt en is beschikbaar voor testruns.
-   De**CONCEPT**-versie kan worden geconverteerd naar een **VOLTOOIDE** versie. Deze versie kan worden gebruikt in lokale rapportageprocessen.
-   De **VOLTOOIDE** versie kan worden geconverteerd naar een **GEDEELDE** versie. Deze versie is gepubliceerd in LCS en kan worden gebruikt in algemene rapportageprocessen.
-   De **GEDEELDE**versie kan worden geconverteerd naar een **VERVALLEN** versie. Deze versie kan vervolgens worden verwijderd.

Versies met de status VOLTOOID of **GEDEELD** zijn beschikbaar voor andere gegevensuitwisseling. Op een onderdeel dat deze statussen heeft kunnen deze acties worden uitgevoerd:

-   Ze kunnen worden geserialiseerd in XML-indeling en geëxporteerd vanuit Dynamics 365 for Operations als bestand in XML-indeling.
-   Ze kunnen opnieuw worden geserialiseerd vanuit een XML-bestand en geïmporteerd in Dynamics 365 for Operations als een nieuwe versie van een ER-onderdeel.

#### <a name="component-date-effectivity"></a>Effectivity van de componentdatum

Versies van ER-onderdelen zijn datumeffectief. De datum**Geldig vanaf**kan worden gedefinieerd voor een ER-onderdeel om de datum op te geven waarop een onderdeel geldig wordt voor rapportageprocessen. De datum van de Dynamics 365 for Operations-sessie wordt gebruikt om te bepalen of een component voor uitvoering geldig is. Als meer dan één versie geldig is voor een specifieke datum, wordt de meest recente versie gebruikt voor rapportageprocessen.

#### <a name="component-access"></a>Componenttoegang

Toegang tot ER-indelingsonderdelen is afhankelijk van de instelling voor de ISO land-/regiocode. Als deze instelling leeg wordt gelaten voor een geselecteerde versie van een indelingsconfiguratie, kan een indelingsonderdeel tijdens de uitvoering worden geopend vanuit elk Dynamics 365 for Operations-bedrijf. Wanneer deze instelling ISO-land/regiocodes bevat, is alleen een indelingscomponent beschikbaar van Dynamics 365 for Operations-bedrijven met een primair adres dat is gedefinieerd voor een van de ISO-land-/regiocodes van een indelingsonderdeel. Verschillende versies van een gegevensindelingsonderdeel kunnen verschillende instellingen hebben voor ISO-land-/regiocodes.

#### <a name="configuration"></a>Configuratie

Een ER-configuratie is de wrapper van een bepaald ER-onderdeel, **Gegevensmodel**of **Indeling**. Een configuratie kan verschillende versies van een bepaald ER-onderdeel bevatten. Elke configuratie is gemarkeerd als eigendom van een bepaalde configuratieprovider. De **CONCEPT**-versie van een onderdeel van een configuratie kan worden bewerkt als de eigenaar van de configuratie als een actieve provider is geselecteerd in de ER-instellingen in Dynamics 365 for Operations. Elke modelconfiguratie bevat een onderdeel **Gegevensmodel**. Een nieuwe indelingsconfiguratie kan afkomstig zijn (worden afgeleid) van een specifieke gegevensmodelconfiguratie. De indelingsconfiguratie die wordt gemaakt wordt gepresenteerd in de configuratiestructuur als een onderliggend element van de oorspronkelijke gegevensmodelconfiguratie. De indelingsconfiguratie die wordt gemaakt bevat een onderdeel **Indeling**. Het onderdeel **Gegevensmodel** van de oorspronkelijke modelconfiguratie wordt automatisch standaard gegevensbron ingevoegd in het onderdeel **Indeling**van de onderliggende indelingsconfiguratie. Een ER-configuratie wordt gedeeld voor Dynamics 365 for Operations-bedrijven.

#### <a name="provider"></a>Aanbieder

De ER-provider is de partij-id die wordt gebruikt om de auteur (eigenaar) van elke ER-configuratie aan te duiden. Via ER kunt u de lijst met configuratieproviders beheren. Indelingsconfiguraties die worden vrijgegeven voor elektronische documenten als onderdeel van de Dynamics 365 for Operations-oplossing zijn gemarkeerd als het eigendom van de configuratieprovider **Microsoft**.

#### <a name="repository"></a>Opslagplaats

In een ER-opslagplaats worden ER-configuraties opgeslagen. De volgende typen ER-opslagplaatsen worden momenteel ondersteund: **Operations-resources** en **LCS-project**. Een opslagplaats Operations-resources biedt toegang tot de lijst met configuraties die als onderdeel van de Dynamics 365 for Operations-oplossing zijn vrijgegeven door Microsoft als ER-configuratieprovider. Deze configuraties kunnen worden geïmporteerd in het huidige exemplaar van Dynamics 365 for Operations en worden gebruikt voor elektronische rapportage. Zij kunnen ook worden gebruikt voor extra lokalisaties/aanpassingen. Een opslagplaats **LCS-project**biedt toegang tot de lijst met configuraties van een specifiek LCS-project (activabibliotheek voor LCS-project) dat is geselecteerd in de fase van registratie van de opslagplaats. Via ER kunt u gedeelde configuraties uploaden vanuit het huidige Dynamics 365 for Operations-exemplaar naar een bepaalde opslagplaats voor **LCS-projecten**. U kunt ook configuraties importeren vanuit een bepaalde opslagplaats voor **LCS-projecten** in het huidige exemplaar van Dynamics 365 for Operations. Vereiste opslagplaatsen voor **LCS-projecten** kunnen afzonderlijk worden geregistreerd voor elke configuratieprovider van het huidige Dynamics 365 for Operations-exemplaar. Elke opslagplaats kan aan een specifieke configuratieprovider zijn gekoppeld.

## <a name="supported-scenarios"></a>Ondersteunde scenario's
### <a name="building-a-data-model"></a>Een gegevensmodel maken

ER biedt een modelontwerper waarmee u een gegevensmodel kunt maken voor een bepaald bedrijfsdomein. Alle domeinspecifieke bedrijfsentiteiten, en de relaties hiertussen, kunnen als een hiërarchische structuur worden voorgesteld in een gegevensmodel. In de volgende afbeelding ziet u een voorbeeld van dit type gegevensmodel (het gegevensmodel van het betalingsdomein). [![Voorbeeld van een gegevensmodel](./media/pic-data-model-1024x550.png)](./media/pic-data-model.png) Speel de taakbegeleider **ER Ontwerp domeinspecifiek gegevensmodel** af (onderdeel van het bedrijfsproces **7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)** om vertrouwd te raken met de details van dit scenario.

### <a name="translating-data-model-content"></a>Inhoud van gegevensmodel vertalen

De inhoud van een gegevensmodel (labels en omschrijvingen) kan worden vertaald in andere talen die in Dynamics 365 for Operations worden ondersteund. Mogelijk wilt u inhoud van een gegevensmodel vertalen om de volgende redenen:

-   Tijdens het ontwerpproces om de inhoud begrijpelijker te maken voor ontwerpers van indelingen die een andere taal spreken en die een gegevensmodel gebruiken voor gegevenstoewijzing van indelingsonderdelen
-   Tijdens de uitvoering, om de inhoud gebruiksvriendelijker te maken door aanwijzingen en help te presenteren voor uitvoeringsparameters en tevens geconfigureerde validatieberichten (fouten en waarschuwingen) in de taal die de voorkeur heeft van de Dynamics 365 for Operations-gebruiker die momenteel is aangemeld.

De volgende afbeelding laat een voorbeeld zien van hoe de inhoud van een gegevensmodel kan worden vertaald vanuit het Engels naar het Japans. [![Gegevensmodelinhoud in het Engels](./media/pic-translate-en-1024x495.png)](./media/pic-translate-en.png)[![Gegevensmodelinhoud vertaald in het Japans](./media/pic-translate-ja-1024x495.png)](./media/pic-translate-ja.png)

### <a name="configuring-data-model-mappings"></a>Gegevensmodeltoewijzingen configureren

ER biedt een ontwerper voor modeltoewijzing waarmee gebruikers gegevensmodellen kunnen toewijzen die zij hebben ontworpen voor specifieke Dynamics 365 for Operations-gegevensbronnen. De volgende afbeelding laat een voorbeeld zien van dit type gegevensmodeltoewijzing (de modeltoewijzing **SEPA-kredietoverdracht** van het domeingegevensmodel voor betaling). [![Voorbeeld van een gegevensmodeltoewijzing ](./media/pic-model-mapping-1024x551.png)](./media/pic-model-mapping.png) Speel de taakbegeleiders **ER Definieer modeltoewijzing en selecteer gegevensbronnen** en **ER Wijs gegevensmodel toe aan geselecteerde gegevensbronnen** (onderdeel van het bedrijfsproces **7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)** af om uzelf vertrouwd te maken met de details van dit scenario.

### <a name="storing-a-designed-model-component-as-a-model-configuration"></a>Een ontworpen modelonderdeel opslaan als modelconfiguratie

ER kan een ontworpen gegevensmodel samen met gekoppelde gegevenstoewijzingen opslaan als een modelconfiguratie van het huidige Dynamics 365 for Operations-exemplaar. In de volgende afbeelding wordt een voorbeeld getoond van dit type gegevensmodelconfiguratie (de configuratie van het betalingsmodel). [![Voorbeeld van een gegevensmodelconfiguratie](./media/pic-model-configuration-1024x585.png)](./media/pic-model-configuration.png) Speel de taakbegeleider **ER Wijs gegevensmodel aan geselecteerde gegevensbronnen toe** af (onderdeel van het bedrijfsproces **7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)** om vertrouwd te raken met de details van dit scenario.

### <a name="building-a-format-that-uses-a-data-model-as-a-base"></a>Een indeling maken die een gegevensmodel als basis gebruikt

ER ondersteunt een indelingsontwerper die u kunt gebruiken om de indeling van een bepaald elektronisch document te maken voor een geselecteerd bedrijfsdomein door het modelonderdeel als basis te selecteren. Dezelfde ER-indelingsontwerper stelt u in staat een indeling als gegevensbron toe te wijzen die u maakt voor de gegevensmodeltoewijzing van een geselecteerd domein. In de volgende afbeelding wordt een voorbeeld weergegeven van dit type indeling (de indelingsconfiguratie die de **BACS**-betalingsindeling voor het Verenigd Koninkrijk ondersteunt). [![Voorbeeld van een indeling die een gegevensmodel als basis heeft](./media/pic-format-1024x690.png)](./media/pic-format.png) Speel de taakbegeleider **ER Ontwerp domeinspecifieke indeling** af (onderdeel van het bedrijfsproces **7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)** om vertrouwd te raken met de details van dit scenario.

### <a name="building-a-configuration-to-generate-electronic-documents-in-openxml-worksheet-format"></a>Een configuratie bouwen voor het genereren van elektronische documenten in OPENXML-werkbladindeling

De indelingsontwerper van ER kan worden gebruikt om een bepaald elektronisch document te maken in OPENXML-werkbladindeling. In de volgende afbeelding wordt een voorbeeld van dit type indeling weergegeven (een indelingsconfiguratie voor het genereren van een OPENXML-werkblad met de details van een geselecteerd betalingsjournaal):[![Pic-ER-format-Excel](./media/pic-er-format-excel.jpg)](./media/pic-er-format-excel.jpg) speel de taakbegeleider **ER Maak een configuratie voor rapporten in OPENXML-indeling** af (onderdeel van het bedrijfsproces **7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)** om vertrouwd te raken met de details van dit scenario). Gebruik het hieronder genoemde Excel-bestand als sjabloon voor het ontwerpen van de ER-indeling om de stap van het importeren van een indelingssjabloon van de taakbegeleider te voltooien: [Sjabloon van betalingsrapport (SampleVendPaymWsReport.xlsx)](https://go.microsoft.com/fwlink/?linkid=845202)

### <a name="storing-a-designed-format-component-in-a-format-configuration"></a>Een ontworpen indelingsonderdeel opslaan in een indelingsconfiguratie

ER kan een ontworpen indeling samen met de geconfigureerde gegevenstoewijzingen opslaan als een indelingsconfiguratie van het huidige Dynamics 365 for Operations-exemplaar. In de voorgaande afbeelding wordt een voorbeeld gegeven van dit type indelingsconfiguratie (**BACS (UK)**, die is een onderliggend element vormt van de configuratie **Betalingsmodel**). Speel de taakbegeleider **ER Ontwerp domeinspecifieke indeling** af (onderdeel van het bedrijfsproces **7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)** om vertrouwd te raken met de details van dit scenario.

### <a name="configuring-dynamics-365-for-operations-to-start-to-use-a-created-format-internally"></a>Dynamics 365 for Operations configureren om een gemaakte indeling intern te gaan gebruiken

Dynamics 365 for Operations kan worden geconfigureerd voor gebruik van een gemaakte indeling om elektronische rapporten te genereren. De verwijzing naar de gemaakte indelingsconfiguratie moet worden gedefinieerd in de instellingen van een specifiek domein. Als u bijvoorbeeld een configuratie in ER-indeling wilt gaan gebruiken voor elektronische betalingen aan leveranciers in BACS-indeling, moet naar de indelingsconfiguratie worden verwezen in specifieke betalingsmethoden, zoals in de volgende afbeeldingen wordt weergegeven: 

[![Configuratie in indeling BACS (UK)](media/ger-bacs-uk-format-configuration.png) 

[![Verwijzen naar de indeling BACS (UK) in een betalingsmethode](media/ger-bacs-uk-format-method.png) 

Speel de taakbegeleiding **ER Gebruik indeling om nieuwe elektronische documenten voor betalingen te genereren** af (onderdeel van het bedrijfsproces **7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)**) om bekend te raken met de details van dit scenario.

## <a name="handling-er-components"></a>ER-onderdelen verwerken
### <a name="publishing-an-er-component-in-lcs-to-offer-it-externally-localization"></a>Een ER-onderdeel publiceren in LCS om dit extern aan te bieden (lokalisatie)

De eigenaar van een onderdeel (model of indeling) dat is gemaakt, kan ER gebruiken voor het publiceren van de voltooide versie van het onderdeel naar LCS. Een opslagplaats van het type **LCS-project**voor de huidige ER-configuratieprovider is vereist. Als de status van de voltooide versie van een onderdeel wordt gewijzigd van **VOLTOOID** naar **GEDEELD**, wordt die versie gepubliceerd in LCS. Wanneer een onderdeel is gepubliceerd naar LCS, wordt de eigenaar van dit onderdeel een provider van de service om het onderdeel te ondersteunen. Als bijvoorbeeld de indelingsonderdeel is ontworpen om een wettelijk vereist elektronisch document te genereren (bijvoorbeeld in overeenstemming met een lokalisatiescenario), wordt ervan uitgegaan dat de indeling in overeenstemming met de wettelijke wijzigingen wordt gehouden en dat de provider nieuwe versies van het onderdeel zal uitgeven telkens wanneer moet worden voldaan aan nieuwe wettelijke vereisten. Speel de taakbegeleider **ER Een configuratie naar Lifecycle Services uploaden**af (onderdeel van het bedrijfsproces **7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)** om vertrouwd te raken met de details van dit scenario.

### <a name="importing-an-er-component-from-lcs-to-use-it-internally"></a>Een ER-onderdeel importeren vanuit LCS om dit intern te maken

Met ER kunt u ER-onderdelen vanuit LCS importeren naar het huidige exemplaar van Dynamics 365 for Operations. Een opslagplaats van het type **LCS-project**is vereist. Wanneer een ER-onderdeel vanuit LCS naar het huidige Dynamics 365 for Operations-exemplaar is geïmporteerd, wordt de eigenaar van het Dynamics AX-exemplaar een consument van de service die door de eigenaar (auteur) van het geïmporteerde onderdeel wordt aangeboden. Als bijvoorbeeld een indelingsonderdeel is ontworpen om vanuit Dynamics 365 for Operations een specifiek elektronisch document te genereren in een bepaalde land-/regiospecifieke indeling (lokalisatiescenario), wordt ervan uitgegaan dat de consument van de service in staat is updates te verkrijgen die worden uitgevoerd voor die indeling om ervoor te zorgen dat de indeling aan de wettelijke vereisten voldoet. Speel de taakbegeleider **ER Een configuratie vanuit Lifecycle Services importeren** af (onderdeel van het bedrijfsproces **7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)** om vertrouwd te raken met de details van dit scenario.

### <a name="building-a-format-selecting-another-format-as-a-base-customization"></a>Een indeling maken door een andere indeling als basis te selecteren (aanpassing)

Met ER kunt u een nieuw (afgeleid) onderdeel maken op basis van de huidige versie van een onderdeel(basis) dat is geïmporteerd vanuit LCS. Stel bijvoorbeeld dat een gebruiker een nieuwe indeling wil afleiden om sommige speciale vereisten voor een elektronisch document te implementeren (zoals een extra veld of een uitgebreide omschrijving) ter ondersteuning van een aanpassingsscenario. Speel de taakbegeleiding **>ER Indeling upgraden door instelling van een nieuwe basis hiervan** af (onderdeel van bedrijfsproces **7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)**) om bekend te raken met de details van dit scenario.

### <a name="upgrading-a-format-selecting-a-new-version-of-base-format-rebase"></a>Een indeling upgraden door een nieuwe versie van de basisindeling (rebase) te selecteren.

Met ER kunt u automatisch wijzigingen in de meest recente versie van het basisondeel aanbrengen in de huidige conceptversie van het afgeleide onderdeel. Dit proces wordt *rebasing* genoemd. Zo kan bijvoorbeeld een nieuwe wijziging in de regelgeving die is geïntroduceerd in de laatste versie van de indeling die werd geïmporteerd vanuit LCS automatisch worden samengevoegd met de aangepaste versie van deze indeling van het elektronisch document. Alle wijzigingen die niet automatisch kunnen worden samengevoegd worden als conflicten beschouwd. Deze conflicten worden weergegeven voor handmatige oplossing in het ontwerpprogramma voor het desbetreffende onderdeel. Speel de taakbegeleiding **>ER Indeling upgraden door instelling van een nieuwe basis hiervan** af (onderdeel van bedrijfsproces **7.5.4.3 Onderdelen voor IT-services en -oplossingen aanschaffen/ontwikkelen (10677)**) om bekend te raken met de details van dit scenario.

## <a name="list-of-er-configurations-that-are-delivered-in-the-dynamics-365-for-operations-solution"></a>Lijst met ER-configuraties die worden geleverd in de Dynamics 365 for Operations-oplossing
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



<a name="see-also"></a>Zie ook
--------

[Lokalisatievereisten – Een configuratie voor elektronische rapportage maken](electronic-reporting-configuration.md)

[De levenscyclus van de configuratie van elektronische rapportage beheren](general-electronic-reporting-manage-configuration-lifecycle.md)




