---
title: Voorraadoverboekingen en correcties uit Field Service synchroniseren met Supply Chain Management
description: In dit onderwerp worden de sjablonen en de onderliggende taken besproken die worden gebruikt om informatie over voorraadcorrecties en -overboekingen te synchroniseren van Dynamics 365 Supply Chain Management met Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 04/30/2019
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
ms.openlocfilehash: ff64f28af570b792f73b51aa9caf06dd2445b2ca
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425328"
---
# <a name="synchronize-inventory-transfers-and-adjustments-from-field-service-to-supply-chain-management"></a>Voorraadoverboekingen en correcties uit Field Service synchroniseren met Supply Chain Management

[!include[banner](../includes/banner.md)]

In dit onderwerp worden de sjablonen en de onderliggende taken besproken die worden gebruikt om informatie over voorraadcorrecties en -overboekingen te synchroniseren van Dynamics 365 Supply Chain Management met Dynamics 365 Field Service.

[![Synchronisatie van zakelijke processen tussen Supply Chain Management en Field Service](./media/FSTransAdjOW.png)](./media/FSTransAdjOW.png)

## <a name="templates-and-tasks"></a>Sjablonen en taken
De volgende sjabloon en onderliggende taken worden gebruikt voor het synchroniseren van voorraadcorrecties en overboekingen vanuit Field Service naar Supply Chain Management.

**Sjablonen in Gegevensintegratie**
- Voorraadcorrectie (Field Service naar Supply Chain Management)
- Voorraadoverboekingen (Field Service naar Supply Chain Management)

**Taak in het project Gegevensintegratie**
- Voorraadcorrecties
- Voorraadoverboekingen

## <a name="entity-set"></a>Entiteitset
| Field Service                     | Supply Chain Management                          |
|-----------------------------------|----------------------------------------------------|
| msdyn_inventoryadjustmentproducts |   Kopteksten en regels van journaalnamen voor CDS-voorraadcorrectie |
| msdyn_inventoryadjustmentproducts | Kopteksten en regels van journaalnamen voor CDS-voorraadoverboeking   |

## <a name="entity-flow"></a>Entiteitstroom
Voorraadcorrecties en -overboekingen die worden uitgevoerd in Field Service, worden gesynchroniseerd met Supply Chain Management nadat de **Boekstatus** van **Gemaakt** is gewijzigd in **Geboekt**. Als dit gebeurt, wordt de correctie- of overboekingsorder vergrendeld en wordt deze alleen-lezen. Dit betekent dat correcties en overboekingen in Supply Chain Management kunnen worden geboekt, maar niet kunnen worden gewijzigd. In Supply Chain Management kunt u een batchtaak instellen om automatisch de correcties te boeken en overboekingsvoorraadjournalen over te boeken die zijn gegenereerd bij de integratie. Zie de volgende vereisten voor meer informatie over het inschakelen van de batchtaak.

## <a name="field-service-crm-solution"></a>Field Service CRM-oplossing 
Het veld **Voorraadeenheid** is toegevoegd aan de entiteit **Product**. Dit veld is vereist omdat de Verkoop- en Voorraadeenheid niet altijd overeenkomt in Supply Chain Management en de Voorraadeenheid nodig is voor de Magazijnvoorraad in Supply Chain Management.
Wanneer u het product voor een voorraadcorrectieproduct instelt voor zowel voorraadcorrecties als voorraadoverboekingen, wordt de eenheid gebaseerd op de voorraadproductwaarde. Als een waarde wordt gevonden, wordt het veld **Eenheid** vergrendeld voor het voorraadcorrectieproduct

Het veld **Boekstatus** is toegevoegd aan zowel de entiteit **Voorraadcorrectie** als de entiteit **Voorraadoverboeking**. Dit veld wordt gebruikt als een filter wanneer een correctie of overboeking wordt verzonden naar Supply Chain Management. De standaardwaarde voor dit veld is Gemaakt (1), maar wordt niet verzonden naar Supply Chain Management. Wanneer u de waarde wijzigt in Geboekt (2), wordt deze verzonden naar Supply Chain Management, maar daarna kunt u de correctie of overboeking niet wijzigen of nieuwe regels toevoegen.

Het veld **Nummerreeks** is toegevoegd aan de entiteit **Voorraadcorrectieproduct**. Dit veld zorgt ervoor dat de integratie een uniek nummer heeft, zodat de correctie kan worden gemaakt en bijgewerkt met de integratie. Wanneer u uw eerste voorraadcorrectieproduct maakt, wordt er een nieuwe record gemaakt in de P2C-entiteit **Automatisch nummeren** om de nummerreeks en het gebruikte voorvoegsel te behouden.

## <a name="prerequisites-and-mapping-setup"></a>Vereisten en instellingen voor toewijzing

### <a name="supply-chain-management"></a>Supply Chain Management
De integratievoorraadjournalen die worden gegenereerd door de integratie, kunnen automatisch worden geboekt met een batchtaak. Dit wordt ingeschakeld via **Voorraadbeheer > Periodieke taken > CDS-integratie > Voorraadjournalen voor integratie boeken**.

## <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

In de volgende afbeeldingen ziet u de sjabloontoewijzing in Gegevensintegratie.

### <a name="inventory-adjustment-field-service-to-supply-chain-management-inventory-adjustment"></a>Voorraadcorrectie (Field Service naar Supply Chain Management): Voorraadcorrectie

[![Sjabloontoewijzing in Gegevensintegratie](./media/FSAdj1.png)](./media/FSAdj1.png)


### <a name="inventory-transfer-field-service-to-supply-chain-management-inventory-transfer"></a>Voorraadoverboeking (Field Service naar Supply Chain Management): Voorraadoverboeking

[![Sjabloontoewijzing in Gegevensintegratie](./media/FSTrans1.png)](./media/FSTrans1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]