---
title: De startpagina Sensor Data Intelligence
description: In dit artikel vindt u een overzicht van Sensor Data Intelligence. Organisaties kunnen met deze functie bedrijfsprocessen aansturen in Microsoft Dynamics 365 Supply Chain Management, op basis van IoT-signalen (Internet of Things) van machines en apparatuur op de werkvloer.
author: johanhoffmann
ms.date: 09/02/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2022-09-02
ms.dyn365.ops.version: 10.0.30
ms.openlocfilehash: 2e4cd8d4d4ffcd10d02fbf26615f12cdd6ccca9e
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428320"
---
# <a name="sensor-data-intelligence-home-page"></a>De startpagina Sensor Data Intelligence

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Met Sensor Data Intelligence voor Microsoft Dynamics 365 Supply Chain Management kunnen organisaties bedrijfsprocessen aansturen in Supply Chain Management, op basis van IoT-signalen (Internet of Things) van machines en apparatuur op de werkvloer. Dit is een bijgewerkte, hernoemde versie van de functie *IoT Intelligence* die eerder beschikbaar was voor Supply Chain Management.

Met Sensor Data Intelligence kunt u de volgende taken uitvoeren:

- Gegevens van machines en apparatuur verzamelen om de waarden van tellers voor onderhoudsactiva in Supply Chain Management bij te werken en om voorspellend onderhoud aan te sturen.
- De oplossing instellen met een eenvoudige wizard voor onboarding in plaats van handmatig componenten te installeren en te configureren in Microsoft Dynamics Lifecycle Services (LCS).
- Onderdelen implementeren op uw eigen abonnement, zodat u meer flexibiliteit hebt bij het beheren van Azure-onderdelen.
- De oplossing configureren, schalen en uitbreiden als bedrijfslogica die op Azure-onderdelen wordt uitgevoerd. Deze onderdelen worden nu in uw eigen abonnement beheerd. U kunt ze dus naar eigen behoeften aanpassen aan uw unieke zakelijke behoeften.

## <a name="business-scenarios"></a>Bedrijfsscenario's

Met Sensor Data Intelligence wordt een aantal typen functionaliteit mogelijk, die elk worden vertegenwoordigd door een specifiek *scenario* in het systeem. Elk scenario biedt een gespecialiseerde set configuratieopties in het systeem, zoals in de volgende tabel wordt beschreven.

| Scenario's | Description |
|---|---|
| [Uitvaltijd voor activum](sdi-scenario-asset-downtime.md) | Houd de efficiëntie van uw machines nauwkeurig bij door middel van sensorgegevens om de uitvaltijd van machines te bewaken. |
| [Activumonderhoud](sdi-scenario-asset-maintenance.md) | Beperk onderhoudskosten en verleng de levensduur van activa door onderhoudsplannen te verbeteren, op basis van sensormeetgegevens van kritieke controlepunten voor machines |
| [Machinestatus](sdi-scenario-equipment-downtime.md) | Borg efficiëntie van uw bedrijfsvoering door met sensormeetgegevens planners te informeren over uitval van machines en opties te bieden voor het verhelpen van mogelijke vertragingen. |
| [Productkwaliteit](sdi-scenario-product-quality.md) | Borg de kwaliteit van productbatches door meetgegevens van sensorern voor werkelijke eigenschappen van elke productbatch te vergelijken, zoals vochtigheid, temperatuur of kwaliteitscriteria die u zelf definieert. Gebruikers worden geïnformeerd over eventuele afwijkingen. |
| [Productievertragingen](sdi-scenario-production-delays.md) | Vergelijk aan de hand van meetgegevens de werkelijke cyclustijd met de geplande cyclustijd en waarschuw supervisors wanneer de productie afwijkt van het schema. Supervisors kunnen vervolgens zo nodig ingrijpen om de efficiëntie van de bewerking te borgen. |

## <a name="architecture"></a>Architectuur

In het volgende architectuurdiagram vindt u een overzicht van de oplossing en de componenten ervan.

![Diagram met de architectuur van Sensor Data Intelligence.](media/sdi-architecture.png "Diagram met de architectuur van Sensor Data Intelligence")
