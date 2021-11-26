---
title: Overzicht van Organisaties en organisatiehiërarchieën
description: Met organisatiehiërarchieën worden de relaties aangegeven tussen de organisaties waaruit het bedrijf bestaat.
author: sericks007
ms.date: 11/10/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: OMHierarchyManager, OMOperatingUnit,
audience: Application User
ms.reviewer: sericks
ms.custom:
- "17291"
- intro-internal
ms.assetid: 76b7ca45-93d4-45cc-b191-66ee63afa1fd
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6f0388b6e7c22c339d26b82c35f1bbb1ef54cdb5
ms.sourcegitcommit: ba10ba2cd4fb4267afb5aacae4f6a52aa2456e7e
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/11/2021
ms.locfileid: "7798341"
---
# <a name="organizations-and-organizational-hierarchies-overview"></a>Overzicht van Organisaties en organisatiehiërarchieën

[!include [banner](../includes/banner.md)]

Een organisatie is een groep mensen die samenwerkt om een bedrijfsproces uit te voeren of een doel te bereiken. Met organisatiehiërarchieën worden de relaties aangegeven tussen de organisaties waaruit het bedrijf bestaat.

## <a name="organizations"></a>Organisaties

U kunt de volgende typen interne organisaties definiëren: rechtspersonen, operationele eenheden en teams.

Alle interne organisaties zijn typen van de entiteit **Partij**. Deze organisaties gebruiken daarom het adresboek om adres- en contactgegevens op te slaan. Een partij kan zowel een persoon als een organisatie zijn en kan tot een of meer adresboeken behoren.

### <a name="legal-entities"></a>Rechtspersonen

Een rechtspersoon is een organisatie met een geregistreerde of wettelijke juridische structuur. Rechtspersonen kunnen wettelijk bindende overeenkomsten aangaan en zijn verplicht prestatieoverzichten te overleggen.

Een bedrijf is een type rechtspersoon. Momenteel zijn bedrijven het enige type rechtspersoon dat u kunt maken. Aan elke rechtspersoon is een bedrijfs-id gekoppeld. Deze koppeling bestaat, omdat in een aantal functionele gebieden in het programma een bedrijfs-ID of gegevensgebieds-ID wordt gebruikt in de gegevensmodellen. In deze functionele gebieden worden bedrijven gebruikt als begrenzing voor gegevensbeveiliging. Gebruikers hebben alleen toegang tot gegevens voor het bedrijf waarbij ze momenteel zijn aangemeld.

### <a name="operating-units"></a>Operationele eenheden

Een operationele eenheid is een organisatie die wordt gebruikt om het beheer van economische middelen en operationele processen in een bedrijf te verdelen. Personen in een operationele eenheid moeten optimaal gebruikmaken van schaarse middelen, processen verbeteren en rekenschap afleggen van hun prestaties.

De typen operationele eenheden omvatten kostenplaatsen, bedrijfseenheden, afdelingen, waardestromen en Commerce-kanalen. De volgende tabel bevat meer informatie over elk type operationele eenheid.

| Type operationele eenheid | Omschrijving | Doel |
|---------------------|-------------|---------|
| Kostenplaats         | Een operationele eenheid waarin managers verantwoordelijk zijn voor de gebudgetteerde en werkelijke uitgaven. | Deze optie wordt gebruikt voor het (operationeel) beheer van bedrijfsprocessen voor alle rechtspersonen. |
| Bedrijfseenheid       | Een semi-zelfstandige operationele eenheid die is gemaakt om strategische doelstellingen van de onderneming te behalen. | Deze optie wordt gebruikt voor financiële rapportages die zijn gebaseerd op industrieën of productlijnen van de organisatie, onafhankelijk van rechtspersonen. |
| Waardestroom        | Een bewerkingseenheid waarmee één of meer productiestromen worden beheerd. | Deze optie wordt vaak gebruikt bij lean manufacturing om de activiteiten en stromen te beheren die zijn vereist voor de levering van een product of service aan klanten. |
| Afdeling          | Een operationele eenheid waarmee een categorie of functioneel onderdeel van een organisatie wordt aangegeven voor het uitvoeren van een specifieke taak, zoals verkoop of boekhouding. | Deze optie wordt gebruikt voor de rapportage over functionele gebieden. Een afdeling kan verantwoordelijk zijn voor winst en verlies en kan bestaan uit een groep kostenplaatsen. |
| Commerce-kanaal      | Een operationele eenheid die een fysieke winkel, een online winkel of een online handelsplaats vertegenwoordigt. | Gebruikt voor het beheer en de operationele controle van een of meer winkels binnen of tussen verschillende rechtspersonen. |

### <a name="teams"></a>Teams

Een team is een organisatie waarin de leden een gemeenschappelijke verantwoordelijkheid, interesse of doelstelling delen. Teams kunnen niet worden gebruikt in organisatiehiërarchieën.

## <a name="organizational-hierarchies"></a>Organisatiehiërarchieën

Hiermee definieert u organisatiehiërarchieën waarmee u verschillende aspecten van uw bedrijf kunt bekijken en hierover kunt rapporteren. U kunt bijvoorbeeld een hiërarchie definiëren met rechtspersonen voor belastingaangifte. U kunt een hiërarchie instellen op basis van operationele eenheden voor het rapporteren over financiële gegevens die niet wettelijk vereist zijn, maar die voor interne controle worden gebruikt. U kunt bijvoorbeeld een inkoophiërarchie maken om inkoopbeleid, regels en bedrijfsprocessen te beheren.

> [!NOTE]
> Nadat een operationele eenheid aan een hiërarchie is toegevoegd, kan de operationele eenheid niet worden verwijderd. 

Aan elke hiërarchie wordt een doel toegewezen. Het doel van een hiërarchie bepaalt welke organisatietypen kunnen worden opgenomen in de hiërarchie. Het doel bepaalt ook de aanvraagscenario's waarbinnen een hiërarchie kan worden gebruikt.

In organisaties in een hiërarchie kunnen parameters, beleid en transacties worden gedeeld. Een organisatie kan de parameters van de bovenliggende organisatie overnemen of vervangen. Gedeelde hoofdgegevens, zoals producten en adresboeken, zijn echter van toepassing op de hele organisatie en kunnen niet worden vervangen voor afzonderlijke organisaties. Voor het maken van organisaties en hiërarchieën is een zorgvuldige planning vereist. Voor meer informatie raadpleegt u [Uw organisatiehiërarchie plannen](plan-organizational-hierarchy.md)

## <a name="additional-resources"></a>Aanvullende bronnen
- [Uw organisatiehiërarchie plannen](plan-organizational-hierarchy.md)
- [Een organisatiehiërarchie maken](tasks/create-organization-hierarchy.md)
- [Een rechtspersoon maken](tasks/create-legal-entity.md)
- [Een operationele eenheid maken](tasks/create-operating-unit.md)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
