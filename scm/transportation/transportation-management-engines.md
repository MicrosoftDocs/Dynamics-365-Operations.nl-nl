---
title: Transportbeheer engines
description: "Transportbeheerengines definiëren de logica die wordt gebruikt om transporttarieven in Transportbeheer te genereren en te verwerken."
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: TMSFreightBillType, TMSGenericEngine, TMSMileageEngine, TMSRateEngine, TMSTransitTimeEngine, TMSZoneEngine
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 12234
ms.assetid: b878478c-0e04-4a1e-a037-6fdbb345a9a3
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-02-28T00:00:00.000Z
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 298ac47e2253f8add1aa3938dda15afe186afbeb
ms.openlocfilehash: c4aac72d9f7e975d4a270deb340f96ddcc9ca1fb
ms.contentlocale: nl-nl
ms.lasthandoff: 06/20/2017

---

# <a name="transportation-management-engines"></a>Transportbeheer engines

[!include[banner](../includes/banner.md)]


Transportbeheerengines definiëren de logica die wordt gebruikt om transporttarieven in Transportbeheer te genereren en te verwerken. 

Een transportbeheer engine berekent taken zoals het transporttarief van de vervoerder. Het enginesysteem staat toe dat u berekeningsstrategieën wijzigt tijdens uitvoeringstijd op basis van gegevens in Microsoft Dynamics 365 for Finance and Operations. Een transportbeheer engine lijkt op een plug-in die aan een bepaald vervoerder contract is gekoppeld.

## <a name="what-engines-are-available"></a>Welke engines zijn beschikbaar?
De volgende tabel bevat de transportbeheerengines die beschikbaar zijn in Microsoft Dynamics 365 for Finance and Operations.

| Transportbeheer engines | Omschrijving                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Tariefengine**                  | Tarieven berekenen.                                                                                                                                                                                                                                                                                                           |
| **Algemene engine**               | Eenvoudige hulpengines die door andere engines worden gebruikt die geen gegevens van Microsoft Dynamics 365 for Finance and Operations vereisen, bijvoorbeeld een toewijzingsengine. De verdelingsengines worden gebruikt om de totaalkosten van transport van specifieke orders en regels te verlagen, gebaseerd dimensies, zoals het volume en gewicht. |
| **Afstandsberekeningsengine**               | Berekent de transportafstand.                                                                                                                                                                                                                                                                                     |
| **Engine voor transittijd**          | Berekent de tijd die vereist is om vanaf het begin naar de eindbestemming te reizen.                                                                                                                                                                                                                                       |
| **Zone-engine**                  | Berekent de zone, gebaseerd op het huidige adres, en berekent het aantal zones dat moet worden gekruist om van adres A naar adres B te reizen.                                                                                                                                                                    |
| **Type vrachtfactuur**            | Standardiseerd de vrachtenfactuur en de vrachtenrekening regels en wordt gebruikt voor het automatische vergelijken van vrachtenrekening.                                                                                                                                                                                                                |

 
<a name="what-engines-must-be-configured-to-rate-a-shipment"></a>Welke engines moet worden geconfigureerd om een zending te beoordelen?
---------------------------------------------------

Om een zending te beoordelen die een specifieke vervoerder gebruikt, moet u meerdere engines van het transportbeheer configureren. De **tariefengine** is vereist, maar andere transportbeheerengines kunnen zijn vereist ter ondersteuning van de **tariefengine**. Zo kan de **tariefengine** bijvoorbeeld worden gebruikt om gegevens op te halen uit de **afstandsberekeningsengine** om het tarief te berekenen op basis van reiskosten tussen bron en bestemming.

## <a name="whats-required-to-initialize-a-transportation-management-engine"></a>Wat is nodig om een transportbeheer engine te initialiseren?
Een transportbeheer engine vereist dat de de initialisering-gegevens instelt om in een specifieke manier te functioneren. De instellingen kan de volgense data types bevatten:
-   Verwijst naar andere transportbeheer engines. Voor details, zie het configuratievoorbeeld in deze sectie.
-   Verwijst naar .NET-typen die de eerste van het transportbeheer worden gebruikt.
-   Simpele configuratiegegevens.

In de meeste gevallen kunt u op de knop **Parameters** in de instellingsformulieren voor de transportbeheerengine klikken om de initialiseringsgegevens te configureren. **Voorbeeld van de configuratie van een tariefengine die verwijst naar een afstandsberekeningsengine** Het volgende voorbeeld toont de instellingen die zijn vereist voor een tariefengine die is gebaseerd op .NET-enginetype Microsoft.Dynamics.Ax.Tms.Bll.MileageRateEngine en verwijst naar een afstandsberekeningsengine.
| Parameter             | Omschrijving                                                                                                                                                                                                                                                                                                                                                                      |
|-----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *RateBaseAssigner*    | Het .NET-type dat de toewijzingsgegevens van de tariefbasis voor een bepaald schema wordt vertaald. De syntaxis van de parameterwaarde bestaat uit twee segmenten die door een verticale streep worden afgebakend (|). Het eerste segment bevat de assemblage-naam die het assigner-type definieert. Het tweede segment definieert het volledig-gekwalificeerde naam van het assigner-type. Dit omvat ook de naamruimte van het type. |
| *MileageEngineCode*   | Code voor de afstandsberekeningsengine die de record voor de afstandsberekeningsengine in de database van Microsoft Dynamics 365 for Finance and Operations identificeert.                                                                                                                                                                                                                                                             |
| *ApportionmentEngine* | Algemene enginecode die de record voor de toewijzingsengine in de database van Microsoft Dynamics 365 for Finance and Operations identificeert.                                                                                                                                                                                                                                                              |

 
<a name="how-is-metadata-used-in-transportation-management-engines"></a>Hoe de metagegevens worden gebruikt in de transportbeheer engines?
----------------------------------------------------------

Transportbeheerengines die afhankelijk zijn van gegevens die zijn gedefinieerd in Dynamics 365 for Finance and Operations kunnen gebruik maken van verschillende gegevensschema's. Het transportbeheersysteem laat toe dat verschillende transportbeheer engines hetzelfde algemene fysieke databasetabellen te gebruiken. Om ervoor te zorgen dat uitvoeringstijd interpretatie van enginegegevens correct is, kunt u voor metagegevens de database-tabellen definiëren. Dit vermindert de kosten om de nieuwe transportbeheerengines te maken omdat geen extra tabel- en formulierstructuren zijn vereist in Dynamics 365 for Operations.

## <a name="what-can-be-used-as-search-data-in-rate-calculations"></a>Wat kan als zoekgegevens in tariefberekeningen worden gebruikt?
De gegevens die u gebruikt wanneer u tarieven in Microsoft Dynamics 365 for Finance and Operations berekent, worden bepaald door de metagegevensconfiguratie. Bijvoorbeeld, als u voor tarieven gebaseerd op postcodes wilt zoeken, moet u metagegevens instellen gebaseerd op oekopdrachttypee van een postcode.

## <a name="do-all-engine-configurations-require-metadata"></a>Hebben alle engineconfiguraties metagegevens nodig?
Nee, de transportbeheer engines die worden gebruikt om de gegevens op te halen, die voor tariefberekening op externe systemen zijn vereist, hebben geen metagegevens nodig. De tariefgegevens voor deze engines kunnen worden opgehaald van de externe systemen van de transport vervoerder, meestal via een webservice. Zo kunt u bijvoorbeeld een afstandsberekeningsengine gebruiken die gegevens direct vanuit Bing-kaarten ophaalt zodat u geen metagegevens voor deze engine nodig hebt.
| **Opmerking**                                                                                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| De transportbeheerengines van het transportbeheer die worden meegeleverd met Finance and Operations, zijn afhankelijk van de gegevens die vanuit de toepassing worden opgehaald. Engines die verbinding maken met externe systemen zijn niet opgenomen met Operations. Echter, het op engines gebaseerde uitbreidbaarheidsmodel maakt het mogelijk om extensies te maken via Microsoft Dynamics 365 for Finance and Operations Visual Studio Tools. |

## <a name="how-do-i-configure-metadata-for-a-transportation-management-engine"></a>Hoe kan ik metagegevens configueren voor een transportbeheer engine?
De metagegevens voor de transportbeheer engines word verschillend geconfigureerd voor de verschillende typen engines.

| Transportbeheer engines               | Metagegevens configuratie:                                                                                                                                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Tariefengine**                                | Vereist een **tariefbasistype**. Het type van de tariefbasis bevat metagegevens voor de gegevens van de tariefbasis en de toewijzingsgegevens van de tariefbasis. Het structuur van de metagegevens van de tariefbasis wordt bepaald door het type tariefengine. De structuur van het tariefbasistype wordt bepaald door het type tariefengine en door het type toewijzing van tariefbasis dat aan de engine is gekoppeld. U kunt het type van de tariefbasis van een tariefengine instellen op de pagina **Tariefengine** en op de pagina **Tariefmodel**. |
| **Zone-engine**                                | Vereist metagegevens om direct op de zone-master te worden ingesteld                                                                                                                                                                                                                                                                                                                                                                                                          |
| **Transittijdengine** en **Afstandsberekeningsengine** | Haalt rechtstreeks de metagegevens op vanuit het instellingenformulier voor configuratie van de afstandberekeningsengine.                                                                                                                                                                                                                                                                                                                                                                                  |

  **Voorbeeld van metagegevens voor een tariefengine** De transportbeheerengine vereist identificatie van het oorsprongsadres, de bestemmingsstatus en het land/regio, en het begin en eindpunt van de zending. Door deze behoeften te gebruiken, ziet de metagegevens er uit zoals de gegevens in het volgende tabel. De tabel bevat ook informatie over wat voor type invoer gegevens vereist zijn.
-   Definieer deze informatie in **Transportbeheer** &gt; **Instellingen** op de pagina **Tariefbasistype**.

| Volgorde | Naam                          | Veldtype | Gegevenstype | Opzoektype    | Verplicht |
|----------|-------------------------------|------------|-----------|----------------|-----------|
| 1        | Herkomst postcode            | Toewijzing | Tekenreeks    | Postcode    | Geselecteerd  |
| 2        | Bestemming Provincie             | Toewijzing | Tekenreeks    | Staat          |           |
| 3        | Bestemming startpunt: postcode | Toewijzing | Tekenreeks    | Postcode    | Geselecteerd  |
| 4        | Bestemming eindpunt: postcode   | Toewijzing | Tekenreeks    | Postcode    | Geselecteerd  |
| 5        | Bestemmingsland           | Toewijzing | Tekenreeks    | Land/regio |           |






