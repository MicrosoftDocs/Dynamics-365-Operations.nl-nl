---
title: Voorraadniveaugegevens vanuit Finance and Operations synchroniseren naar Field Service
description: Dit onderwerp bespreekt de sjablonen en de onderliggende taken die worden gebruikt om informatie op voorraadniveau te synchroniseren van Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 01/14/2019
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
ms.openlocfilehash: b81694f1ed56d8542de46203ac5faf5fae2b6645
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/29/2019
ms.locfileid: "356778"
---
# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a>Informatie over voorraadniveau uit Finance and Operations synchroniseren met Field Service 

[!include[banner](../includes/banner.md)]

Dit onderwerp bespreekt de sjablonen en de onderliggende taken die worden gebruikt om informatie op voorraadniveau te synchroniseren van Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service.

[![Synchronisatie van zakelijke processen tussen Finance and Operations en Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>Sjablonen en taken
De volgende sjabloon en onderliggende taken worden gebruikt om beschikbare voorraadniveaus te synchroniseren van Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service.

**Sjabloontoewijzing in Gegevensintegratie**
- Productvoorraad (Finance and Operations naar Field Service)
  
**Taak in het project Gegevensintegratie**
- Productvoorraad

De volgende synchronisatietaken moeten worden uitgevoerd voordat de synchronisatie van voorraadniveaus kan plaatsvinden:
- Magazijnen (Finance and Operations naar Field Service) 
- Field Service-producten met Voorraadeenheid (Finance and Operations naar Sales) 

## <a name="entity-set"></a>Entiteitset

| Field Service                      | Finance en Operations                 |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | Voorhanden CDS-voorraad per magazijn     |

## <a name="entity-flow"></a>Entiteitstroom
Voorraadniveaugegevens worden vanuit Finance and Operations naar Field Service verzonden voor geselecteerde producten. Voorraadniveaugegevens bevatten: 
- Voorhanden hoeveelheid (huidige geregistreerde fysieke hoeveelheid in het magazijn)
- Hoeveelheid in bestelling (totale geregistreerde hoeveelheid in bestelling, zoals verkooporders)
- Bestelde hoeveelheid (totale geregistreerde bestelde hoeveelheid, zoals inkooporders)

Deze gegevens worden per vrijgegeven product geregistreerd voor elk magazijn en gesynchroniseerd op basis van wijzigingstracering wanneer het voorraadniveau verandert.

In Field Service worden met de integratieoplossing voorraadjournalen voor de delta gemaakt om ervoor te zorgen dat de niveaus in Field Service overeenkomen met de niveaus in Finance and Operations.

Finance and Operations fungeert als master voor voorraadniveaus. Daarom is het belangrijk om de integratie voor werkorders, overboekingen en correcties van Field Service naar Finance and Operations in te stellen als deze functionaliteit wordt gebruikt in Field Service. Daarnaast moeten voorraadniveaus vanuit Finance and Operations worden gesynchroniseerd.

De producten en magazijnen waarvoor voorraadniveaus worden gemaakt via Finance and Operations kunnen worden beheerd met Geavanceerde Query en filtering (Power Query).

> [!NOTE]
> Het is mogelijk om meerdere magazijnen in Field Services te maken (met **Wordt extern beheerd = Nee**) en deze toe te wijzen aan één magazijn in Finance and Operations, met de functies voor geavanceerde query's en filters. Dit wordt gebruikt in situaties waarin u wilt dat Field Service het gedetailleerde voorraadniveau beheert en alleen updates verzendt naar Finance and Operations. In dit geval ontvangt Field Service geen updates over voorraadniveaus van Finance and Operations. Zie voor meer informatie [Voorraadcorrecties vanuit Field Service synchroniseren naar Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) en [Werkorders in Field Service synchroniseren met verkooporders in Finance and Operations](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="field-service-crm-solution"></a>Field Service CRM-oplossing
De entiteit **Externe productvoorraad** is een nieuwe entiteit die alleen voor de back-end wordt gebruikt in de integratie. Deze entiteit ontvangt de voorraadniveauwaarden uit Finance and Operations tijdens de integratie en transformeert die waarden vervolgens in journalen voor handmatige voorraad waarmee vervolgens de voorraadproducten in het magazijn worden gewijzigd.

## <a name="prerequisites-and-mapping-setup"></a>Vereisten en instellingen voor toewijzing

### <a name="data-integration-project"></a>Gegevensintegratieproject
U kunt filters toepassen met Geavanceerde query en filtering zodat dat alleen bepaalde producten en magazijnen vanuit Finance and Operations naar Field Service worden verzonden.

## <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a>Productvoorraad (Finance and Operations naar Field Service): Productvoorraad

[![Sjabloontoewijzing in Gegevensintegratie](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)
