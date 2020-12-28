---
title: Projectlijsten uit Supply Chain Management synchroniseren met Field Service
description: In dit onderwerp worden de sjablonen en de onderliggende taken besproken die worden gebruikt om projecten te synchroniseren van Dynamics 365 Supply Chain Management met Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: d80fce409ee92973a6134d96ce839b9722980918
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425111"
---
# <a name="synchronize-project-list-from-supply-chain-management-to-field-service"></a>Projectlijsten uit Supply Chain Management synchroniseren met Field Service

[!include[banner](../includes/banner.md)]

In dit onderwerp worden de sjablonen en de onderliggende taken besproken die worden gebruikt om projecten te synchroniseren van Dynamics 365 Supply Chain Management met Dynamics 365 Field Service.

[![Synchronisatie van zakelijke processen tussen Supply Chain Management en Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>Sjablonen en taken
De volgende sjabloon en onderliggende taken worden gebruikt voor het synchroniseren van projecten vanuit Supply Chain Management naar Field Service.

**Sjabloontoewijzing in Gegevensintegratie**
- Projecten (Supply Chain Management naar Field Service)

**Taak in het project Gegevensintegratie**
- Projecten

De volgende synchronisatietaken moeten worden uitgevoerd voordat de synchronisatie van een projectlijst kan plaatsvinden:
- Rekeningen (Sales naar Supply Chain Management) 

## <a name="entity-set"></a>Entiteitset
| Field Service           | Supply Chain Management  |
|-------------------------|-------------------------|
|msdynce_externalprojects | Projecten                |

## <a name="entity-flow"></a>Entiteitstroom
Projecten worden gemaakt in Supply Chain Management. Projecten met **Tijd en materiaal** als **Projecttype** en **Onderhanden** als **Projectfase** worden gesynchroniseerd met de entiteit **Extern project** in Field Service, inclusief informatie over het projectnummer, de projectnaam, de projectfase en de klantrekening. De lijst **Extern project** wordt gebruikt om Field Service-werkorders te koppelen aan Supply Chain Management-projecten.

## <a name="field-service-crm-solution"></a>Field Service CRM-oplossing
De entiteit **Extern project** ontvangt alle projecten van Supply Chain Management. Het veld **Extern project** is toegevoegd aan de entiteit **Werkorder**. Dit veld is een opzoekveld, dus wanneer u uw werkorder aan een project koppelt, wordt de verkooporder verbonden met een project in Supply Chain Management. Nadat de **Systeemstatus** van **Geopend - In uitvoering (690.970.000)** in een hogere status wordt gewijzigd, wordt het veld **Extern project** vergrendeld en kunt u de waarde niet meer toevoegen, verwijderen of wijzigen.

## <a name="prerequisites-and-mapping-setup"></a>Vereisten en instellingen voor toewijzing
### <a name="supply-chain-management"></a>Supply Chain Management
Wijzigingen bijhouden voor gegevensentiteitprojecten inschakelen

## <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie


### <a name="projects-supply-chain-management-to-field-service-projects"></a>Projecten (Supply Chain Management naar Field Service): Projects

[![Sjabloontoewijzing in Gegevensintegratie](./media/FSProject1.png)](./media/FSProject1.png)
