---
title: Technische bedrijven en regels voor gegevenseigendom
description: In dit onderwerp wordt uitgelegd hoe u een of meer technische bedrijven kunt gebruiken om ervoor te zorgen dat de hoofdgegevens voor producten centraal worden gemaakt en onderhouden. Een technisch bedrijf staat voor het bedrijf dat eigenaar is van de technische producten en de technisch relevante gegevens.
author: t-benebo
manager: tfehr
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EngChgEngineeringOrganization
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: 5cab02600e13a1a539b5ae0cd3ff66960430e826
ms.sourcegitcommit: 5f21cfde36c43887ec209bba4a12b830a1746fcf
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/29/2020
ms.locfileid: "4425891"
---
# <a name="engineering-companies-and-data-ownership-rules"></a>Technische bedrijven en regels voor gegevenseigendom

[!include [banner](../includes/banner.md)]

## <a name="engineering-companies-and-operational-companies"></a>Technische bedrijven en operationele bedrijven

U kunt een of meer *technische bedrijven* gebruiken om ervoor te zorgen dat de hoofdgegevens voor producten centraal worden gemaakt en onderhouden. Een technisch bedrijf is eigenaar van de technische producten en de bijbehorende technisch relevante gegevens. Het is altijd verbonden met (gebaseerd op) een bestaande *rechtspersoon*, wat ook een bedrijf is. Via deze verbinding brengt het systeem een centraal toegangspunt tot stand voor alle technisch relevante gegevens over technische producten in het technische bedrijf. In dit centrale toegangspunt worden technische producten gemaakt en technisch relevante gegevens beheerd. Van hieruit worden de technische producten en technisch relevante gegevens vrijgegeven aan *operationele bedrijven*, die andere rechtspersonen zijn. (Zie [Productstructuren van de vrijgave](release-product-structure.md) voor meer informatie over het vrijgavebeheer.) Deze operationele bedrijven gebruiken de technische gegevens zoals deze zijn ontworpen door het technische bedrijf. Alle logistieke gegevens worden lokaal beheerd door elk technisch bedrijf en operationeel bedrijf.

Ga naar **Technisch wijzigingsbeheer \> Instellen \> Technische organisaties** als u een technisch bedrijf wilt maken. Selecteer **Nieuw**, voer een naam in voor het technische bedrijf en selecteer het bestaande bedrijf (rechtspersoon) waarop het is gebaseerd.

Als u een integratie met PLM-systemen (systemen voor productlevenscyclusbeheer) hebt, moet u een bedrijfseenheid (bedrijfstype) maken die een extern bedrijf wordt.

## <a name="engineering-product-categories-and-engineering-companies"></a>Categorieën van technische producten en technische bedrijven

Met *categorieën voor technische producten* worden technische producten gemaakt volgens de bedrijfsregels van uw bedrijf en gedragen deze zich zoals nodig is. Zie [Technische versies en categorieën van technische producten](engineering-versions-product-category.md) voor meer informatie over categorieën voor technische producten.

Elke categorie voor technische producten behoort tot een specifiek technisch bedrijf en kan alleen producten maken die tot dat bedrijf behoren. Op dezelfde manier behoort het recht om een technisch product te onderhouden ook toe aan het bedrijf dat is gekoppeld aan de categorie voor technische producten van dat product.

## <a name="data-that-is-owned-by-the-engineering-company"></a>Gegevens die het eigendom zijn van het technische bedrijf

Aangezien het technische bedrijf eigenaar is van de technisch relevante gegevens, heeft dit bedrijf controle over de volgende processen:

- **Het maken van technische producten:** elk technisch bedrijf kan alleen nieuwe technische producten maken die zijn gebaseerd op een categorie voor technische producten waarvan deze eigenaar is. In sommige gevallen behouden operationele bedrijven hun eigen lokale gegevens die betrekking hebben op die producten.
- **Het maken van technische versies:** wanneer een bedrijf een nieuw technisch product maakt, wordt automatisch een eerste technische versie hiervoor gemaakt. Alleen het technische bedrijf dat eigenaar is, kan nieuwe versies van dat product maken.
- **Het maken en onderhouden van technische kenmerken:** wanneer een bedrijf een nieuw technisch product maakt, worden er automatisch technische kenmerken aan toegevoegd. Alleen het technische bedrijf dat de eigenaar is, kan de waarden voor die kenmerken maken en onderhouden. Zie [Technische kenmerken en de zoekfunctie voor technische kenmerken](engineering-attributes-and-search.md) voor meer informatie over technische kenmerken.
- **Het maken en onderhouden van stuklijsten die zijn verbonden met de technische versies:** het technische bedrijf dat eigenaar is, kan een stuklijst rechtstreeks verbinden met een versie van een technisch product. Wanneer deze stuklijsten worden vrijgegeven aan andere rechtspersonen, worden wijzigingen in de technische gegevens voor de stuklijsten op de volgende manieren beperkt:

    - Het operationele bedrijf kan vrijgegeven stuklijstregels niet verwijderen.
    - De technische velden op de stuklijstregels zijn alleen-lezen voor het operationele bedrijf. Alle andere velden zijn logistieke implementatievelden en kunnen worden bewerkt door het operationele bedrijf.
    - Het operationele bedrijf kan stuklijstregels toevoegen aan dezelfde stuklijst. Op deze manier kunnen lokale toevoegingen, zoals verpakkingsmateriaal of smeervloeistoffen, worden toegevoegd.
    - Het operationele bedrijf kan een geheel nieuwe, lokale stuklijst toevoegen. Deze wijziging is mogelijk vereist in gevallen waarin bijvoorbeeld geen stuklijst wordt geleverd tijdens de vrijgave. Het operationele bedrijf is eigenaar van deze lokale stuklijsten en beheert deze. Zie [Productstructuren van de vrijgave](release-product-structure.md) voor meer informatie over vrijgavebeheer.
    - Alle lokale stuklijsten en stuklijstregels blijven behouden wanneer het technische bedrijf de stuklijst bijwerkt.

- **Het maken en onderhouden van routes die zijn verbonden met de technische versies:** het technische bedrijf kan een route rechtstreeks verbinden met elke versie van een technisch product. Wanneer deze routes worden vrijgegeven aan andere rechtspersonen, worden wijzigingen in de gegevens voor de routes op de volgende manieren beperkt:

    - De andere rechtspersonen kunnen de technische gegevens op de routes niet verwijderen.
    - De andere rechtspersonen kunnen bewerkingen toevoegen aan de route. Op deze manier kunnen ze lokale routestappen toevoegen.
    - Operationele bedrijven kunnen geheel nieuwe, lokale routes toevoegen. Deze wijziging is mogelijk vereist als u bijvoorbeeld geen routes hebt opgenomen tijdens de vrijgave. de operationele bedrijven zijn eigenaar van deze lokale routes en beheren deze. Zie [Productstructuren van de vrijgave](release-product-structure.md) voor meer informatie over vrijgavebeheer.
    - Alle lokale wijzigingen blijven behouden wanneer updates van het technische bedrijf weer worden vrijgegeven naar de routes.

- **Het maken en onderhouden van technische documenten:** het technische bedrijf kan technische documenten koppelen aan elke technische versie.

    - Wanneer deze documenten aan andere rechtspersonen worden vrijgegeven, worden de documenten beschermd tegen verwijdering door het operationele bedrijf.
    - Andere rechtspersonen kunnen volledig nieuwe lokale documenten toevoegen. Het operationele bedrijf is eigenaar van deze lokale documenten en beheert deze.
