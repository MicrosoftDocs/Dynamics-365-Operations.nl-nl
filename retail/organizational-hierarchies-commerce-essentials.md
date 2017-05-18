---
title: "Organisaties en organisatiehiërarchieën (Hoofdzaken van commerce)"
description: "Hoofdzaken van commerce kent drie typen interne organisaties die u kunt definiëren, om een organisatie te helpen een bedrijfsproces uit te voeren of een doelstelling te bereiken."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 21251
ms.assetid: 2bfc6bfe-784b-42e8-8bf0-116e9f0a558e
ms.search.region: global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: 50d29b6552cf7af5f2d9296b1d70b838a8edd637
ms.contentlocale: nl-nl
ms.lasthandoff: 04/26/2017


---

# <a name="organizations-and-organizational-hierarchies-commerce-essentials"></a>Organisaties en organisatiehiërarchieën (Hoofdzaken van commerce)

[!include[banner](includes/banner.md)]


Hoofdzaken van commerce kent drie typen interne organisaties die u kunt definiëren, om een organisatie te helpen een bedrijfsproces uit te voeren of een doelstelling te bereiken. 

Een organisatie is een groep mensen die samenwerken om een bedrijfsproces uit te voeren of een doel te bereiken. Een organisatiehiërarchie geeft de relaties weer tussen de bedrijfseenheden waaruit uw organisatie bestaat.

## <a name="organizations"></a>Organisaties
In Hoofdzaken van commerce kunt u drie typen interne organisaties definiëren: rechtspersonen, operationele eenheden en teams. In Microsoft Dynamics AX zijn alle interne organisaties typen van de entiteit Partij. Deze organisaties gebruiken daarom een adresboek om adressen en andere contactgegevens op te slaan. Een partij kan zowel een persoon als een organisatie zijn en kan tot een of meer adresboeken behoren.
### <a name="legal-entities"></a>Rechtspersonen

Een rechtspersoon is een organisatie met een geregistreerde of wettelijke juridische structuur. Rechtspersonen kunnen wettelijk bindende overeenkomsten aangaan en zijn verplicht prestatieoverzichten te overleggen. Een bedrijf is een soort rechtspersoon in Microsoft Dynamics AX en elke rechtspersoon is aan een bedrijfs-id gekoppeld. Deze koppeling bestaat omdat een bedrijfs-id, of DataAreaId, wordt gebruikt in sommige gegevensmodellen waar de bedrijven worden gebruikt als begrenzing voor gegevensbeveiliging. Gebruikers hebben alleen toegang tot gegevens voor het bedrijf waarbij ze momenteel zijn aangemeld.

### <a name="operating-units"></a>Operationele eenheden

Een operationele eenheid is een organisatie die wordt gebruikt om het beheer van economische middelen en operationele processen in een bedrijf te verdelen. Personen in een operationele eenheid moeten optimaal gebruikmaken van schaarse middelen, processen verbeteren en rekenschap afleggen van hun prestaties. Voorbeelden van typen operationele eenheden in Hoofdzaken van commerce zijn kostenplaatsen, bedrijfseenheden, afdelingen, waardestromen en detailhandelkanalen. De volgende tabel bevat meer informatie over elk type operationele eenheid.
|                         |                                                                                         |                                                                                                                                             |
|-------------------------|-----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| **Type bedrijfsonderdeel** | **Omschrijving**                                                                         | **Doel**                                                                                                                                 |
| Bedrijfseenheid           | Een semi-zelfstandige operationele eenheid die is gemaakt om strategische doelstellingen van de onderneming te behalen. | Gebruik bedrijfseenheden voor financiële rapportages die zijn gebaseerd op industrieën of productlijnen van de organisatie, onafhankelijk van rechtspersonen. |
| Detailhandelafzetkanaal          | Een operationele eenheid die een fysieke winkel vertegenwoordigt.                             | Hiermee kunt u een of meerdere winkels beheren en regelen binnen of over rechtspersonen.                                                               |

## <a name="organizational-hierarchies"></a>Organisatiehiërarchieën
Aan elke hiërarchie wordt een doel in toegewezen in Hoofdzaken van commerce. Het doel van een hiërarchie bepaalt welke organisatietypen kunnen worden opgenomen in de hiërarchie. Het doel bepaalt ook de aanvraagscenario's waarbinnen een hiërarchie kan worden gebruikt. Een detailhandelhiërarchie kan bijvoorbeeld worden gebruikt om producten te kopen en verkopen in een winkel. In organisaties in een hiërarchie kunnen parameters, beleid en transacties worden gedeeld. Een organisatie kan de parameters van de bovenliggende organisatie overnemen of vervangen. Gedeelde hoofdgegevens, zoals producten en adresboeken, zijn echter van toepassing op de hele organisatie en kunnen niet worden vervangen voor afzonderlijke organisaties.
### <a name="best-practices-for-setting-up-an-organization-in-a-hierarchy"></a>Beste praktijken voor het instellen van een organisatie in een hiërarchie

Houd rekening met de volgende beste praktijken wanneer u een organisatiehiërarchie implementeert:
-   Maak een afdeling om de doorsnede tussen een rechtspersoon en een bedrijfseenheid te specificeren. U kunt vervolgens gegevens vergaderen van een afdeling naar een rechtspersoon voor wettelijke aangiften en van een afdeling naar een bedrijfseenheid voor interne rapportage.
-   Stel geen meerdere hiërarchieën in voor hetzelfde hiërarchiedoel in één rechtspersoon.
-   Maak geen hiërarchie voor elk doel. Gewoonlijk kunt u één hiërarchie voor meerdere doelen gebruiken. Eén hiërarchie van operationele eenheden kan bijvoorbeeld aan alle beleidsdoelen worden toegewezen.
-   Gebalanceerde hiërarchieën maken. In een hiërarchie worden alle knooppunten die zich op dezelfde afstand van het basisknooppunt bevatten als een niveau gedefinieerd. In een gebalanceerde hiërarchie kan slechts één type operationele eenheid voorkomen op elk niveau en de afstand tussen het basisknooppunt en het niveau is consistent. Als er tussenniveaus zijn tussen een afdeling en een rechtspersoon of bedrijfseenheid, zijn er mogelijk placeholderorganisaties vereist om een gebalanceerde hiërarchie te maken.
-   Stel geen afzonderlijke hiërarchie in van operationele eenheden als de structuur voor rechtspersonen ook uw operationele structuur is. Een gemengde hiërarchie van rechtspersonen en operationele eenheden kan voor beide doeleinden worden gebruikt.
-   Voordat u belangrijke herstructureringsscenario's instelt, gebruikt u de ingangsdatums van de hiërarchie om een impactanalyse en een validatietest uit te voeren.
-   Sla een hiërarchie op als concept als u een hiërarchie mogelijk wijzigt voordat u deze hebt gepubliceerd.
-   Beperk het aantal mensen met machtigingen om organisaties toe te voegen of te verwijderen uit een hiërarchie in een productieomgeving. Een kleiner aantal beperkt de kans dat kostbare fouten optreden en correcties moeten worden uitgevoerd.

## <a name="retail-store-management"></a>Beheer van detailhandelwinkel
De volgende tabel beschrijft de scenario's van Hoofdzaken van commerce waar de organisatiehiërarchieën kunnen worden gebruikt.
| Opdracht                                                                           | Beschrijving                                                                                                                                                                                                                                                                                                | Hiërarchiedoel    |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|
| Detailhandelassortiment managen                                                      | Identificeer de producten die beschikbaar zijn in elke detailhandelwinkel.                                                                                                                                                                                                                                             | Detailhandelassortiment    |
| Beheer aanvulling detailhandel                                                    | Groepeer winkels voor aanvulling voorraad gebaseerd op aanvullingsregels.                                                                                                                                                                                                                                          | Aanvulling detailhandel |
| Rapporteer gegevens voor winkels                                                         | Groepeer winkels voor rapportage.                                                                                                                                                                                                                                                                                | Detailhandelrapportage     |
| Boek voorraad, bereken overzichten, of boek overzichten voor een groep winkels | Maak een groep winkels die aan een batchtaak kunnen worden toegewezen. Wanneer u een batchtaak definieert om voorraad te boeken, overzichten te berekenen of overzichten te boeken, kunt u opgeven op welke hiërarchie de taak van toepassing is. Wanneer winkels worden toegevoegd of verwijderd uit de hiërarchie, hoeft u de batchtaak niet te wijzigen. | POS-boekingen detailhandel   |






