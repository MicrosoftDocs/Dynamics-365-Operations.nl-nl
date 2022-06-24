---
title: Onderdelen van elektronische rapportage
description: In dit artikel worden de onderdelen van elektronische rapportage (ER) beschreven.
author: nselin
ms.date: 09/28/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.topic: overview
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c2b8b197fdea0cd49fc5161a12b8f547cc1a27bf
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8892445"
---
# <a name="electronic-reporting-components"></a>Onderdelen van elektronische rapportage

[!include [banner](../includes/banner.md)]

Elektronische rapportage (ER) ondersteunt de volgende typen onderdelen:

- Gegevensmodel
- Modeltoewijzing
- Format
- Metagegevens

## <a name="data-model-component"></a>Gegevensmodelcomponent

Een gegevensmodelonderdeel is een abstracte representatie van een gegevensstructuur. Hiermee wordt een specifiek bedrijfsdomeingebied beschreven met voldoende details om te voldoen aan de rapportagevereisten voor dat domein. Een gegevensmodelonderdeel bestaat uit de volgende elementen:

- **Gegevensmodel** – Een set domeinspecifieke bedrijfsentiteiten en een hiërarchisch gestructureerde definitie van relaties tussen die entiteiten.
- **Modeltoewijzing** – Geselecteerde toepassingsgegevensbronnen worden gekoppeld aan individuele elementen van een gegevensmodel waarmee tijdens runtime de gegevensstroom en regels voor het invullen van bedrijfsgegevens in een gegevensmodelonderdeel worden gedefinieerd.

De bedrijfsentiteit van een gegevensmodel wordt voorgesteld als een container of record. Bedrijfsonderdeeleigenschappen worden weergegeven als gegevensitems of velden. Elk gegevensitem heeft een unieke naam, label, omschrijving en waarde. De waarde van elk gegevensitem kan zodanig worden ontworpen dat deze wordt herkend als een tekenreeks, geheel getal, reëel getal, datum, opsomming of een Booleaanse waarde. Bovendien kan het gegevensitem een andere record of een lijst met records zijn.

Een enkel gegevensmodelonderdeel kan verschillende hiërarchieën met domeinspecifieke zakelijke entiteiten bevatten. Het gegevensitem kan ook modeltoewijzingen bevatten, die ondersteuning bieden voor een bepaalde rapportspecifiek gegevensstroom tijdens runtime. De hiërarchieën worden onderscheiden op basis van een enkele record die is geselecteerd als basis voor modeltoewijzing. Zo ondersteunt bijvoorbeeld het gegevensmodel van het gebied van het betalingsdomein mogelijk de volgende toewijzingen:


- Bedrijf \> Leverancier \> Betalingstransacties van het debiteurendomein
- Klant \> Bedrijf \> Betalingstransacties van het crediteurendomein

Zakelijke entiteiten, zoals bedrijf en betalingstransacties, worden slechts één keer ontworpen. Verschillende toewijzingen kunnen ze indien nodig opnieuw gebruiken.

## <a name="model-mapping-component"></a>Modeltoewijzingsonderdeel

Met modeltoewijzing worden toepassingsgegevensbronnen gekoppeld aan individuele elementen van een gegevensmodel waarmee tijdens de uitvoering de gegevensstroom en regels voor het invullen van bedrijfsgegevens in een gegevensmodelonderdeel worden gedefinieerd.

Een modeltoewijzing die ondersteuning biedt voor uitgaande elektronische documenten, heeft de volgende mogelijkheden:

- Er kunnen verschillende gegevenstypen worden gebruikt als gegevensbronnen voor een gegevensmodel. Deze gegevenstypen omvatten tabellen, gegevensentiteiten, methoden en opsommingen.
- Er worden gebruikersinvoerparameters ondersteund die kunnen worden gedefinieerd als gegevensbronnen voor een gegevensmodel wanneer bepaalde gegevens moeten worden opgegeven tijdens runtime.
- Er wordt ondersteuning geboden voor de transformatie van gegevens in de vereiste groepen. U kunt gegevens ook filteren, sorteren en gegevens optellen en logische berekende velden toevoegen die zijn ontwikkeld door middel van formules die vergelijkbaar zijn met Microsoft Excel-formules. Zie voor meer informatie het onderwerp [Formuleontwerper in elektronische rapportage (ER)](general-electronic-reporting-formula-designer.md).

Een modeltoewijzing die ondersteuning biedt voor inkomende elektronische documenten, heeft de volgende mogelijkheden:

- Deze kan verschillende bij te werken gegevenselementen als doel gebruiken. Deze gegevenselementen omvatten tabellen, gegevensentiteiten en weergaven. De gegevens kunnen worden bijgewerkt door inkomende gegevens van elektronische documenten. In een enkele modeltoewijzing kunnen meerdere doelen worden gebruikt.
- Er worden gebruikersinvoerparameters ondersteund die kunnen worden gedefinieerd als gegevensbronnen voor een gegevensmodel wanneer bepaalde gegevens moeten worden opgegeven tijdens runtime.

Een gegevensmodelonderdeel is ontworpen voor elk bedrijfsdomein dat wordt gebruikt als uniforme gegevensbron voor rapportage. De uniforme gegevensbron isoleert rapportage vanuit de fysieke implementatie van gegevensbronnen. Het onderdeel vertegenwoordigt domeinspecifieke zakelijke concepten en functionaliteit in een indeling die het initiële ontwerp en later onderhoud van een rapportageformulier efficiënter maakt.

## <a name="format-component"></a>Indelingscomponent

### <a name="format-components-for-outgoing-electronic-documents"></a>Indelingscomponent voor uitgaande elektronische documenten

Een indelingsonderdeel is het schema van de rapportage-uitvoer die wordt gegenereerd tijdens runtime. Een schema bestaat uit de volgende elementen:

- Een indeling die de structuur en de inhoud definieert van het uitgaande document voor elektronische rapportage dat wordt gegenereerd tijdens runtime.
- Gegevensbronnen, als een reeks van gebruikersinvoerparameters en een domeinspecifiek gegevensmodel dat een geselecteerde modeltoewijzing gebruikt
- Een indelingstoewijzing, als reeks van bindingen van indelingsgegevensbronnen die individuele elementen bevatten van een indeling die tijdens runtime de gegevensstroom en de regels voor het genereren van de indelingsuitvoer specificeert.
- Een indelingsvalidatie, als een reeks configureerbare regels die de het genereren van het rapport tijdens runtime controleren, afhankelijk van de uitvoeringscontext. Zo kan er bijvoorbeeld een regel zijn die het genereren van betalingen van een leverancier onderbreekt en een uitzondering genereert, wanneer specifieke kenmerken van de geselecteerde leverancier ontbreken, zoals het bankrekeningnummer.

Een indelingsonderdeel ondersteunt de volgende functies:

- Het maken van rapportage-uitvoer als afzonderlijke bestanden in verschillende indelingen, zoals tekst, XML, Microsoft Word-document of werkblad
- Het maken van meerdere afzonderlijke bestanden en het opnemen van die bestanden in zip-bestanden

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


## <a name="component-versioning"></a>Componentversiebeheer

Versiebeheer wordt ondersteund voor ER-onderdelen. De volgende werkstroom voorziet in het beheer van wijzigingen in ER-onderdelen:

1. De versie die oorspronkelijk is gemaakt, wordt gemarkeerd als een **Concept**-versie. Deze versie kan worden bewerkt en is beschikbaar voor testruns.
2. De **Concept**-versie kan worden geconverteerd naar een **Voltooide** versie. Deze versie kan worden gebruikt in lokale rapportageprocessen.
3. De **Voltooide** versie kan worden geconverteerd naar een **Gedeelde** versie. Deze versie is gepubliceerd in Microsoft Dynamics Lifecycle Services (LCS) en kan worden gebruikt in algemene rapportageprocessen.
4. De **Gedeelde** versie kan worden geconverteerd naar een **Vervallen** versie. Deze versie kan worden verwijderd.

Versies met de status **Voltooid** of **Gedeeld** zijn beschikbaar voor andere gegevensuitwisseling. Op onderdelen met een van deze statussen kunnen deze acties worden uitgevoerd:

- Het onderdeel kan worden geserialiseerd in XML-indeling en geëxporteerd als bestand in XML-indeling.
- Een component kan opnieuw worden geserialiseerd vanuit een XML-bestand en geïmporteerd de toepassing als een nieuwe versie van een ER-onderdeel.

## <a name="component-date-effectivity"></a>Effectivity van de componentdatum

Versies van ER-onderdelen zijn datumeffectief. U kunt de datum Geldig vanaf' definiëren voor een ER-onderdeel om de datum op te geven waarop een onderdeel geldig wordt voor rapportageprocessen. De datum van toepassingssessie wordt gebruikt om te definiëren of een onderdeel geldig is voor uitvoering. Als meer dan één versie geldig is voor een specifieke datum, wordt de meest recente versie gebruikt voor rapportageprocessen.

## <a name="component-access"></a>Componenttoegang

Toegang tot componenten van de ER-indeling is afhankelijk van de instelling voor de ISO-land-/regiocode (International Organization for Standardization). Als deze instelling leeg is voor een geselecteerde versie van een indelingsconfiguratie, kan een indelingsonderdeel tijdens runtime worden geopend vanuit elk bedrijf. Als de instelling ISO-land-/regiocodes bevat, is alleen een indelingscomponent beschikbaar van bedrijven met een primair adres dat is gedefinieerd voor een van de ISO-land-/regiocodes van een indelingsonderdeel.

Verschillende versies van een gegevensindelingsonderdeel kunnen verschillende instellingen hebben voor ISO-land-/regiocodes.

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

