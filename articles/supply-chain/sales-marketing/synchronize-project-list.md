---
title: Projectlijst vanuit Finance and Operations synchroniseren naar Field Service
description: In dit onderwerp komen de sjablonen en onderliggende taken voor het synchroniseren van projecten vanuit Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service aan de orde.
author: ChristianRytt
manager: AnnBe
ms.date: 12/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.translationtype: HT
ms.sourcegitcommit: 8c6cb481f1a3fe48d329c5936118d8df88a4175b
ms.openlocfilehash: adcb1c1b241ce2b073cd26cf2a8a8d64931c8b0f
ms.contentlocale: nl-nl
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a>Projectlijst vanuit Finance and Operations synchroniseren naar Field Service

[!include[banner](../includes/banner.md)]

In dit onderwerp komen de sjablonen en onderliggende taken voor het synchroniseren van projecten vanuit Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service aan de orde.

[![Synchronisatie van zakelijke processen tussen Finance and Operations en Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>Sjablonen en taken
De volgende sjabloon en onderliggende taken worden gebruikt voor het synchroniseren van projecten vanuit Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service.

**Naam van de sjabloon in Gegevensintegratie:**
- Projecten (Finance and Operations naar Field Service)

**Namen van de taken in het project Gegevensintegratie:**
- Projecten

De volgende synchronisatietaken moeten worden uitgevoerd voordat de synchronisatie van een projectlijst kan plaatsvinden:
- Rekeningen (Sales naar Finance and Operations) 

## <a name="entity-set"></a>Entiteitset
Field Service   Finance and Operations

| Field Service           | Finance en Operations  |
|-------------------------|-------------------------|
|msdynce_externalprojects | Projecten                |

## <a name="entity-flow"></a>Entiteitstroom
Projecten worden gemaakt in Finance and Operations. Projecten met Tijd en materiaal als **projecttype** en Onderhanden als **projectfase** orden gesynchroniseerd naar de entiteit **Extern project** in Field Service, inclusief informatie over het projectnummer, de projectnaam, de projectfase en de klantrekening. De lijst **Extern project** wordt gebruikt om Field Service-werkorders te koppelen aan Finance and Operations-projecten.
De Field Service CRM-oplossing Het externe project is een nieuwe entiteit die alle projecten uit Operations krijgt.
Het veld Extern project is toegevoegd aan de entiteit Werkorder. Dit veld is een opzoekveld en wanneer u uw werkorder aan een project koppelt, wordt de verkooporder verbonden met een project in Operations. Zodra de systeemstatus van Geopend - In uitvoering (690.970.000) in een hogere status wordt gewijzigd, wordt het veld Extern project vergrendeld en kunt u de waarde niet toevoegen, verwijderen of wijzigen.

## <a name="prerequisites-and-mapping-setup"></a>Vereisten en instellingen voor toewijzing
### <a name="in-finance-and-operations"></a>In Finance and Operations
Wijzigingen bijhouden voor gegevensentiteitprojecten inschakelen

## <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie


### <a name="projects-finance-and-operations-to-field-service-projects"></a>Projecten (Finance and Operations naar Field Service): Projecten

[![Sjabloontoewijzing in Gegevensintegratie](./media/FSProject1.png)](./media/FSProject1.png)

