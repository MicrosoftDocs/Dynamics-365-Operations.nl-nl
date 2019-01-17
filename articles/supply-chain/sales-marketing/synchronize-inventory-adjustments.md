---
title: Voorraadoverboekingen en -correcties vanuit Field Service synchroniseren naar Finance and Operations
description: In dit onderwerp komen de sjablonen en onderliggende taken voor het synchroniseren van voorraadcorrecties en -overboekingen vanuit Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service aan de orde.
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
ms.openlocfilehash: 79a1cfac3fa94223cc9af73e758ce95fd47065c9
ms.contentlocale: nl-nl
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a>Voorraadcorrecties vanuit Field Service synchroniseren naar Finance and Operations

[!include[banner](../includes/banner.md)]

In dit onderwerp komen de sjablonen en onderliggende taken voor het synchroniseren van voorraadcorrecties en -overboekingen vanuit Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service aan de orde.

[![Synchronisatie van zakelijke processen tussen Finance and Operations en Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>Sjablonen en taken
De volgende sjabloon en onderliggende taken worden gebruikt voor het synchroniseren van voorraadcorrecties en -overboekingen vanuit Microsoft Dynamics 365 for Field Service naar Microsoft Dynamics 365 for Finance and Operations.

**Naam van de sjablonen in Gegevensintegratie:**
- Voorraadcorrectie (Field Service naar Finance and Operations)
- Voorraadoverboekingen (Field Service naar Finance and Operations)

**Namen van de taken in de projecten Gegevensintegratie:**
- Voorraadcorrecties
- Voorraadoverboekingen

## <a name="entity-set"></a>Entiteitset
| Field Service                     | Finance en Operations                             |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts |   Kopteksten en regels van journaalnamen voor CDS-voorraadcorrectie |
| msdyn_inventoryadjustmentproducts | Kopteksten en regels van journaalnamen voor CDS-voorraadoverboeking   |

## <a name="entity-flow"></a>Entiteitstroom
Voorraadcorrecties en -overboekingen die worden uitgevoerd in Field Service worden gesynchroniseerd naar Finance and Operations wanneer **Boekstatus** van Gemaakt is gewijzigd in Geboekt. Wanneer dit gebeurt, wordt de correctie- of overboekingsorder vergrendeld en alleen-lezen, aangezien correcties en overboekingen in Finance and Operations kunnen worden geboekt en dus niet kunnen worden gewijzigd.
In Finance and Operations kunt u een batchverwerking instellen om automatisch de correcties te boeken en de voorraadjournalen over te boeken die zijn gegenereerd bij de integratie. Zie de vereiste hieronder voor meer informatie over het inschakelen van de batchtaak.

## <a name="field-service-crm-solution"></a>Field Service CRM-oplossing 
Het veld Voorraadeenheid is toegevoegd aan de entiteit Product. Dit veld is vereist omdat de verkoop- en voorraadeenheid niet altijd overeenkomen in Operations en voor de magazijnvoorraad in Operations de voorraadeenheid nodig is.
Wanneer u het product voor een voorraadcorrectieproduct instelt voor zowel voorraadcorrecties als voorraadoverboekingen, wordt de eenheid gebaseerd op het voorraadproduct. Als een waarde wordt gevonden, wordt het veld Eenheid vergrendeld voor het voorraadcorrectieproduct

Het veld Boekstatus is toegevoegd aan de entiteit Voorraadcorrectie en de entiteit Voorraadoverdracht. Dit veld wordt gebruikt als een filter voor wanneer een correctie of overboeking wordt verzonden naar Operations. Het veld wordt standaard ingesteld op Gemaakt (1) en wordt vervolgens niet verzonden naar Operations. Wanneer u dit wijzigt in Geboekt (2), wordt dit verzonden naar Operations. In dat geval kunt u niets meer wijzigen in de correctie of overboeking of nieuwe regels toevoegen.
Het veld Nummerreeks is toegevoegd aan de entiteit Voorraadcorrectieproduct. Hierdoor heeft de integratie een uniek nummer op basis waarvan kan worden bepaald of iets moet worden gemaakt of bijgewerkt. Wanneer u uw eerste voorraadcorrectieproduct maakt, wordt er een nieuwe record gemaakt in de P2C-entiteit Automatisch nummeren om de nummerreeks en het gebruikte voorvoegsel te behouden.

## <a name="prerequisites-and-mapping-setup"></a>Vereisten en instellingen voor toewijzing

### <a name="in-finance-and-operations"></a>In Finance and Operations
De integratievoorraadjournalen die worden gegenereerd door de integratie kunnen automatisch worden geboekt met een batchtaak. Dit wordt ingeschakeld via: Voorraadbeheer > Periodieke taken > CDS-integratie > Voorraadjournalen voor integratie boeken

## <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

In de volgende afbeeldingen ziet u de sjabloontoewijzing in Gegevensintegratie.

### <a name="inventory-adjustment-field-service-to-finance-and-operations-inventory-adjustment"></a>Voorraadcorrectie (Field Service naar Finance and Operations): Voorraadcorrectie

[![Sjabloontoewijzing in Gegevensintegratie](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-finance-and-operations-inventory-transfer"></a>Voorraadoverboeking (Field Service naar Finance and Operations): Voorraadoverboeking

[![Sjabloontoewijzing in Gegevensintegratie](./media/FSTrans1.png)](./media/FSTrans1.png)

