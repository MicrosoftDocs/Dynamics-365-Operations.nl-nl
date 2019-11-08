---
title: Voorraadjournalen
description: In dit onderwerp wordt beschreven hoe u voorraadjournalen kunt gebruiken om diverse typen fysieke voorraadtransacties te boeken.
author: perlynne
manager: AnnBe
ms.date: 04/05/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventJournalBOM, InventJournalCount, InventJournalCountTag, InventJournalLossProfit, InventJournalMovement, InventJournalTransfer, WMSJournalTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 51631
ms.assetid: 3fedeaaf-502f-483c-93d2-ab266828189e
ms.search.region: Global
ms.author: mafoge
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1c4a2696b015611f4430ad5dfa1c61c1c4f913a9
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/10/2019
ms.locfileid: "2570789"
---
# <a name="inventory-journals"></a>Voorraadjournalen

[!include [banner](../includes/banner.md)]

In dit onderwerp wordt beschreven hoe u voorraadjournalen kunt gebruiken om diverse typen fysieke voorraadtransacties te boeken.

De voorraadjournalen in Supply Chain Management worden gebruikt om fysieke voorraadtransacties van diverse typen te boeken, zoals het boeken van uitgiften en ontvangsten, voorraadmutaties, het maken van stuklijsten (BOMs), en de afstemming van fysieke voorraad. Al deze voorraadjournalen worden gebruikt op een vergelijkbare manier, maar ze worden onderscheiden in verschillende typen.

## <a name="types-of-inventory-journals"></a>Typen voorraadjournalen
De volgende voorraadjournaaltypen zijn beschikbaar:

-   Mutatie
-   Voorraadcorrectie
-   Overboeken
-   Stuklijst
-   Artikelontvangst
-   Productie-invoer
-   Tellen
-   Telling labels

### <a name="movement"></a>Mutatie

Wanneer u een voorraadmutatiejournaal gebruikt, kunt u kosten aan een artikel toevoegen wanneer u voorraad toevoegt, maar u moet handmatig de extra kosten aan een bepaalde grootboekrekening toewijzen door een grootboektegenrekening op te geven wanneer u het journaal maakt. Dit voorraadjournaaltype is handig als u de standaardrekeningen wilt overschrijven.

### <a name="inventory-adjustment"></a>Voorraadcorrectie

Wanneer u een voorraadcorrectiejournaal gebruikt, kunt u kosten aan een artikel toevoegen wanneer u voorraad toevoegt. De extra kosten worden automatisch naar een bepaalde grootboekrekening geboekt, op basis van de instellingen van het boekingsprofiel van de artikelengroep. Gebruik dit voorraadjournaaltype om voorraadwinsten en -verliezen bij te werken, wanneer het artikel zijn standaardtegenrekening van het grootboek moet houden. Wanneer u een voorraadcorrectiejournaal boekt, wordt een voorraadontvangst of -uitgifte geboekt, wordt de waarde van de voorraad gewijzigd en worden grootboektransacties gegenereerd.

### <a name="transfer"></a>Overboeken

U kunt overboekingsjournalen gebruiken om artikelen tussen voorraadlocaties, batches, of productvarianten te boeken, zonder kostenimplicaties te koppelen. U kunt bijvoorbeeld artikelen van het ene magazijn naar een ander magazijn in hetzelfde bedrijf overboeken. Wanneer u een overboekingsjournaal gebruikt, moet u de dimensies "van" en "naar" beide opgeven (bijvoorbeeld, voor Locatie en Magazijn). De voorhanden voorraad voor de gedefinieerde voorraaddimensie wordt dienovereenkomstig bijgewerkt. Voorraadoverboekingen reflecteren de onmiddellijke verplaatsing van materiaal. Transitvoorraad wordt niet getraceerd. Als transitvoorraad moet worden gevolgd, kunt u in plaats daarvan beter een transferorder gebruiken. Wanneer u een overboekingsjournaal boekt, worden twee voorraadtransacties gemaakt voor elke journaalregel:

-   Een voorraaduitgifte op de "van"-locatie.
-   Een voorraadontvangst op de "aan"-locatie.

### <a name="bom"></a>Stuklijst

Wanneer u stuklijst als voltooid rapporteert, kunt u een BOM-journaal maken. Met behulp van een stuklijstdagboek kunt u de stuklijst rechtstreeks boeken. Deze boeking genereert een voorraadontvangst van het product, samen met een gekoppelde stuklijst en een voorraaduitgifte van de producten op de stuklijst. Dit voorraadjournaaltype is nuttig in zowel eenvoudige productiescenario's als scenario's met grote volumes, waarbij routes niet zijn vereist.

### <a name="item-arrival"></a>Artikelontvangst

U kunt het artikelontvangstjournaal gebruiken om de ontvangst van artikelen (bijvoorbeeld van inkooporders) te registreren. Een artikelontvangstjournaal kan worden gemaakt als onderdeel van het ontvangstbeheer op de pagina **Ontvangstoverzicht**, of u kunt handmatig een journaalpost maken op de pagina **Artikelontvangst**. Als u de artikelontvangstjournaalnaam inschakelt voor controle van orderverzamellocaties, wordt in Supply Chain Management een locatie voor de ontvangen artikelen gezocht. Als er ruimte is, worden de locatiebestemmingen voor binnenkomende artikelen gegenereerd.

### <a name="production-input"></a>Productie-invoer

De journalen voor productie-invoer werken als de artikelontvangstjournalen, maar worden voor productieorders gebruikt.

### <a name="counting"></a>Tellen

De tellijsten laten u de huidige voorhanden voorraad corrigeren die voor artikelen of groepen artikelen is geregistreerd, en boeken dan de werkelijke materiële telling zodat u de correcties kunt maken die nodig zijn om de verschillen af te stemmen. U kunt telbeleid koppelen aan telgroepen om artikelen te groeperen die uiteenlopende kenmerken hebben, zodat die artikelen in een teljournaal kunnen worden opgenomen. U kunt bijvoorbeeld telgroepen configureren om artikelen te tellen die een specifieke frequentie hebben, of om artikelen te tellen wanneer de voorraad daalt tot een bepaald niveau. Zie voor informatie over het definiëren van telgroepen [Voorraadtellingsprocessen definiëren (taakbegeleider)](tasks/define-inventory-counting-processes.md).

### <a name="tag-counting"></a>Telling labels

Labeltellijsten worden gebruikt om een genummerd label aan een tellingspartij toe te wijzen. Het label moet een labelnummer, een artikelnummer, en de hoeveelheid van het artikel bevatten. Om ervoor te zorgen dat een label slechts eenmalig wordt gebruikt en dat alle labels worden gebruikt, moet elk artikelnummer een unieke set labels hebben met zijn eigen nummerreeks. Drie statuswaarden kunnen voor elk label worden ingesteld:

-   **Gebruikt**: Het artikelnummer wordt geteld voor dit label.
-   **Ongeldig gemaakt**: Het artikelnummer wordt ongeldig gemaakt voor dit label.
-   **Ontbreekt**: Het artikelnummer ontbreekt voor dit label.

Wanneer u een labeltellijst boekt, wordt een nieuwe tellijst gemaakt op basis van de regels van de labeltellijst. Voor meer informatie over labeltelling, zie [Voorraadlabeltelling](inventory-tag-counting.md).

## <a name="working-with-journals"></a>Werken met dagboeken
Een journaalregel is alleen toegankelijk voor één gebruiker tegelijk. Als verschillende gebruikers tegelijkertijd toegang tot de journalen nodig hebben om journaalregels te maken, moeten de gebruikers journalen selecteren die momenteel niet worden gebruikt om te voorkomen dat gegevens worden overschreven. In gevallen waarin meerdere afdelingen hetzelfde journaaltype gebruiken, is het handig om meerdere journaalnamen (bijvoorbeeld één per afdeling) te maken. Het kan ook handig zijn om journalen op te delen, zodat elke boekingsroutine in een eigen, uniek voorraadjournaal wordt ingevoerd. Voor boekingsroutines die zijn gekoppeld aan voorraadtransacties maakt u een journaal voor periodieke voorraadcorrecties en een ander journaal voor voorraadtelling.

## <a name="posting-journal-lines"></a>Journaalregels boeken
U kunt op elk gewenst moment de journaalregels boeken die u maakt, tot u een artikel van extra transacties hebt vergrendeld. De gegevens die u in een journaal invoert, blijven in dat journaal bewaard, zelfs als u het journaal sluit zonder de regels te boeken.

## <a name="data-entity-support-for-inventory-journals"></a>Ondersteuning van gegevensentiteit voor voorraadjournalen

Gegevensentiteiten ondersteunen de volgende typen integratiescenario's:
-    Synchrone service (OData)
-  Asynchrone integratie

Zie [Gegevensentiteiten](../../dev-itpro/data-entities/data-entities.md) voor meer informatie.

> [!NOTE]
> Niet alle voorraadjournalen ondersteunen OData, dus u kunt de Excel-gegevensconnector niet gebruiken om gegevens te publiceren, bij te werken en terug te importeren in Supply Chain Management. 

Een ander verschil tussen de journaalgegevensentiteiten is de mogelijkheid om samengestelde entiteiten te gebruiken met kop- en regelgegevens. Op dit moment kunt u de samengestelde entiteiten gebruiken voor:
-   Voorraadcorrectiejournaal
-   Voorraadmutatiejournaal

Deze twee voorraadjournalen ondersteunen alleen het scenario *Voorraad initialiseren* als onderdeel van het importeren van een gegevensbeheerproject:
-  Wanneer geen journaalnummer voor de koptekst is opgegeven, maar een nummerreeks voor het journaaltype is opgegeven, worden met de importtaak automatisch journaalkopteksten per 1000 regels gemaakt. Bijvoorbeeld resulteert het importeren van 2020 regels in de volgende drie kopteksten:
    -  Kop 1: bevat 1000 regels
    -  Kop 2: bevat 1000 regels
    -  Kop 3: bevat 20 regels
-  Hierbij wordt ervan uitgegaan dat unieke regelgegevens bestaan per voorraaddimensie; dit kan een product-, opslag- en traceringsdimensie zijn. Daarom is het niet mogelijk om journaalregels te importeren, waarvoor alleen het datumveld verschilt op de regels binnen hetzelfde importproject.

## <a name="additional-resources"></a>Aanvullende resources

[Gegevensentiteiten](../../dev-itpro/data-entities/data-entities.md)
