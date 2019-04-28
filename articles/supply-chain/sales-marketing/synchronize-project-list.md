---
title: Projectlijst vanuit Finance and Operations synchroniseren naar Field Service
description: In dit onderwerp worden de sjablonen en de onderliggende taken besproken die worden gebruikt om projecten te synchroniseren van Microsoft Dynamics 365 for Finance and Operations met Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: ea5c188891bb97ba73d2d022e86bbff50897381b
ms.sourcegitcommit: a6d385db6636ef2b7fb6b24d37a2160c8d5a3c0f
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/14/2019
ms.locfileid: "842599"
---
# <a name="synchronize-project-list-from-finance-and-operations-to-field-service"></a>Projectlijst van Finance and Operations synchroniseren met Field Service

[!include[banner](../includes/banner.md)]

In dit onderwerp worden de sjablonen en de onderliggende taken besproken die worden gebruikt om projecten te synchroniseren van Microsoft Dynamics 365 for Finance and Operations met Microsoft Dynamics 365 for Field Service.

[![Synchronisatie van zakelijke processen tussen Finance and Operations en Field Service](./media/FSProjectOW.png)](./media/FSProjectOW.png)

## <a name="templates-and-tasks"></a>Sjablonen en taken
De volgende sjabloon en onderliggende taken worden gebruikt om projecten te synchroniseren van Microsoft Dynamics 365 for Finance and Operations met Microsoft Dynamics 365 for Field Service.

**Sjabloontoewijzing in Gegevensintegratie**
- Projecten (Fin and Ops naar Field Service)

**Taak in het project Gegevensintegratie**
- Projecten

De volgende synchronisatietaken moeten worden uitgevoerd voordat de synchronisatie van een projectlijst kan plaatsvinden:
- Rekeningen (Sales naar Fin and Ops) 

## <a name="entity-set"></a>Entiteitset
| Field Service           | Finance en Operations  |
|-------------------------|-------------------------|
|msdynce_externalprojects | Projecten                |

## <a name="entity-flow"></a>Entiteitstroom
Projecten worden gemaakt in Finance and Operations. Projecten met **Tijd en materiaal** als **Projecttype** en **Onderhanden** als **Projectfase** worden gesynchroniseerd met de entiteit **Extern project** in Field Service, inclusief informatie over het projectnummer, de projectnaam, de projectfase en de klantrekening. De lijst **Extern project** wordt gebruikt om Field Service-werkorders te koppelen aan Finance and Operations-projecten.

## <a name="field-service-crm-solution"></a>Field Service CRM-oplossing
De entiteit **Extern project** ontvangt alle projecten van Finance and Operations. Het veld **Extern project** is toegevoegd aan de entiteit **Werkorder**. Dit veld is een opzoekveld. Dus wanneer u uw werkorder aan een project koppelt, wordt de verkooporder verbonden met een project in Finance and Operations. Nadat de **Systeemstatus** van **Geopend - In uitvoering (690.970.000)** in een hogere status wordt gewijzigd, wordt het veld **Extern project** vergrendeld en kunt u de waarde niet meer toevoegen, verwijderen of wijzigen.

## <a name="prerequisites-and-mapping-setup"></a>Vereisten en instellingen voor toewijzing
### <a name="finance-and-operations"></a>Finance en Operations
Wijzigingen bijhouden voor gegevensentiteitprojecten inschakelen

## <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie


### <a name="projects-fin-and-ops-to-field-service-projects"></a>Projecten (Fin and Ops naar Field Service): Projecten

[![Sjabloontoewijzing in Gegevensintegratie](./media/FSProject1.png)](./media/FSProject1.png)
