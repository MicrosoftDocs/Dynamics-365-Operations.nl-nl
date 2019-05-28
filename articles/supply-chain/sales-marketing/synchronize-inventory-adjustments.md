---
title: Voorraadoverboekingen en -correcties vanuit Field Service synchroniseren naar Finance and Operations
description: In dit onderwerp worden de sjablonen en de onderliggende taken besproken die worden gebruikt om informatie over voorraadcorrecties en -overboekingen te synchroniseren van Microsoft Dynamics 365 for Finance and Operations met Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 04/30/2019
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
ms.openlocfilehash: e94fa87c2f8b66574d6c5b2930cebf2e1b144fea
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2019
ms.locfileid: "1536291"
---
# <a name="synchronize-inventory-adjustments-from-field-service-to-finance-and-operations"></a>Voorraadcorrecties vanuit Field Service synchroniseren naar Finance and Operations

[!include[banner](../includes/banner.md)]

In dit onderwerp worden de sjablonen en de onderliggende taken besproken die worden gebruikt om informatie over voorraadcorrecties en -overboekingen te synchroniseren van Microsoft Dynamics 365 for Finance and Operations met Microsoft Dynamics 365 for Field Service.

[![Synchronisatie van zakelijke processen tussen Finance and Operations en Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>Sjablonen en taken
De volgende sjabloon en onderliggende taken worden gebruikt om voorraadcorrecties en -overboekingen te synchroniseren van Microsoft Dynamics 365 for Field Service met Microsoft Dynamics 365 for Finance and Operations.

**Sjablonen in Gegevensintegratie**
- Voorraadcorrectie (Field Service naar Fin en Ops)
- Voorraadoverboekingen (Field Service naar Fin en Ops)

**Taak in het project Gegevensintegratie**
- Voorraadcorrecties
- Voorraadoverboekingen

## <a name="entity-set"></a>Entiteitset
| Field Service                     | Finance en Operations                             |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts |   Kopteksten en regels van journaalnamen voor CDS-voorraadcorrectie |
| msdyn_inventoryadjustmentproducts | Kopteksten en regels van journaalnamen voor CDS-voorraadoverboeking   |

## <a name="entity-flow"></a>Entiteitstroom
Voorraadcorrecties en -overboekingen die worden uitgevoerd in Field Service, worden gesynchroniseerd met Finance and Operations nadat **Boekstatus** van **Gemaakt** is gewijzigd in **Geboekt**. Als dit gebeurt, wordt de correctie- of overboekingsorder vergrendeld en wordt deze alleen-lezen. Dit betekent dat correcties en overboekingen in Finance and Operations kunnen worden geboekt, maar niet kunnen worden gewijzigd. In Finance and Operations kunt u een batchtaak instellen om automatisch de correcties te boeken en overboekingsvoorraadjournalen over te boeken die zijn gegenereerd bij de integratie. Zie de volgende vereisten voor meer informatie over het inschakelen van de batchtaak.

## <a name="field-service-crm-solution"></a>Field Service CRM-oplossing 
Het veld **Voorraadeenheid** is toegevoegd aan de entiteit **Product**. Dit veld is vereist omdat de verkoop- en voorraadeenheid niet altijd overeenkomt in Finance and Operations en de voorraadeenheid is nodig voor de magazijnvoorraad in Finance and Operations.
Wanneer u het product voor een voorraadcorrectieproduct instelt voor zowel voorraadcorrecties als voorraadoverboekingen, wordt de eenheid gebaseerd op de voorraadproductwaarde. Als een waarde wordt gevonden, wordt het veld **Eenheid** vergrendeld voor het voorraadcorrectieproduct

Het veld **Boekstatus** is toegevoegd aan zowel de entiteit **Voorraadcorrectie** als de entiteit **Voorraadoverboeking**. Dit veld wordt gebruikt als een filter wanneer een correctie of overboeking wordt verzonden naar Finance and Operations. De standaardwaarde voor dit veld is Gemaakt (1), maar wordt niet verzonden naar Finance and Operations. Wanneer u de waarde wijzigt in Geboekt (2), wordt deze verzonden naar Finance and Operations, maar daarna kunt u de correctie of overboeking niet wjzigen of nieuwe regels toevoegen.

Het veld **Nummerreeks** is toegevoegd aan de entiteit **Voorraadcorrectieproduct**. Dit veld zorgt ervoor dat de integratie een uniek nummer heeft, zodat de correctie kan worden gemaakt en bijgewerkt met de integratie. Wanneer u uw eerste voorraadcorrectieproduct maakt, wordt er een nieuwe record gemaakt in de P2C-entiteit **Automatisch nummeren** om de nummerreeks en het gebruikte voorvoegsel te behouden.

## <a name="prerequisites-and-mapping-setup"></a>Vereisten en instellingen voor toewijzing

### <a name="finance-and-operations"></a>Finance en Operations
De integratievoorraadjournalen die worden gegenereerd door de integratie, kunnen automatisch worden geboekt met een batchtaak. Dit wordt ingeschakeld via **Voorraadbeheer > Periodieke taken > CDS-integratie > Voorraadjournalen voor integratie boeken**.

## <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

In de volgende afbeeldingen ziet u de sjabloontoewijzing in Gegevensintegratie.

### <a name="inventory-adjustment-field-service-to-fin-and-ops-inventory-adjustment"></a>Voorraadcorrectie (Field Service naar Fin and Ops): Voorraadcorrectie

[![Sjabloontoewijzing in Gegevensintegratie](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-fin-and-ops-inventory-transfer"></a>Voorraadoverboeking (Field Service naar Fin and Ops): Voorraadoverboeking

[![Sjabloontoewijzing in Gegevensintegratie](./media/FSTrans1.png)](./media/FSTrans1.png)
