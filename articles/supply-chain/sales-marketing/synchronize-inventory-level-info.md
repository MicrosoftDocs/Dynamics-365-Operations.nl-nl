---
title: Voorraadniveaugegevens vanuit Finance and Operations synchroniseren naar Field Service
description: In dit onderwerp komen de sjablonen en onderliggende taken voor het synchroniseren van voorraadniveaugegevens vanuit Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service aan de orde.
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
ms.openlocfilehash: 3ccc4d406fa4f9800dcdf8697a91892408783196
ms.contentlocale: nl-nl
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-inventory-level-information-from-finance-and-operations-to-field-service"></a>Voorraadniveaugegevens vanuit Finance and Operations synchroniseren naar Field Service 

[!include[banner](../includes/banner.md)]

In dit onderwerp komen de sjablonen en onderliggende taken voor het synchroniseren van voorraadniveaugegevens vanuit Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service aan de orde.

[![Synchronisatie van zakelijke processen tussen Finance and Operations en Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>Sjablonen en taken
De volgende sjabloon en onderliggende taken worden gebruikt voor het synchroniseren van voorhanden voorraadniveaus vanuit Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service.

**Naam van de sjabloon in Gegevensintegratie:**
- Productvoorraad (Finance and Operations naar Field Service)
  
**Namen van de taken in het project Gegevensintegratie:**
- Productvoorraad

De volgende synchronisatietaken moeten worden uitgevoerd voordat de synchronisatie van voorraadniveaus kan plaatsvinden:
- Magazijnen (Finance and Operations naar Field Service) 
- Field Service-producten met Voorraadeenheid (Finance and Operations naar Sales) 

## <a name="entity-set"></a>Entiteitset

| Field Service                      | Finance en Operations                 |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | Voorhanden CDS-voorraad per magazijn     |

## <a name="entity-flow"></a>Entiteitstroom
Voorraadniveaugegevens worden vanuit Finance and Operations naar Field Service verzonden voor bepaalde producten. Voorraadniveaugegevens bevatten onder andere informatie over het volgende: 
- Voorhanden hoeveelheid (huidige geregistreerde fysieke hoeveelheid in het magazijn)
- Hoeveelheid in bestelling (totale geregistreerde hoeveelheid in bestelling, d.w.z. verkooporders)
- Bestelde hoeveelheid (totale geregistreerde bestelde hoeveelheid, d.w.z. inkooporders)

Deze gegevens worden per vrijgegeven product geregistreerd voor elk magazijn en gesynchroniseerd op basis van wijzigingstracering wanneer het voorraadniveau verandert.

In Field Service worden met de integratieoplossing voorraadjournalen voor de delta gemaakt om ervoor te zorgen dat de niveaus in Field Service overeenkomen met de niveaus in Finance and Operations.

Finance and Operations fungeert als master voor voorraadniveaus. Daarom is het belangrijk om de integratie voor werkorders, overboekingen en correcties van Field Service naar Finance and Operations in te stellen als deze functionaliteit wordt gebruikt in Field Service. Daarnaast moeten voorraadniveaus vanuit Finance and Operations worden gesynchroniseerd.

De producten en magazijnen waarvoor voorraadniveaus worden gemaakt via Finance and Operations kunnen worden beheerd met Geavanceerde Query en filtering (Power Query).

Opmerking: het is mogelijk om meerdere magazijnen in Field Services te maken (met Wordt extern beheerd = Nee) en deze toe te wijzen aan één magazijn in Finance and Operations, met de functies voor geavanceerde query's en filters. Dit wordt gebruikt in situaties waarin u wilt dat Field Service het gedetailleerde voorraadniveau maakt en alleen updates verzendt naar Finance and Operations. In dit geval ontvangt Field Service geen updates over voorraadniveaus van Finance and Operations. Zie Voorraadcorrecties vanuit Field Service synchroniseren naar Finance and Operations en Werkorders in Field Service synchroniseren met verkooporders in Finance and Operations voor meer informatie.

## <a name="field-service-crm-solution"></a>Field Service CRM-oplossing
De entiteit Externe productvoorraad is een nieuwe entiteit die alleen voor de back-end wordt gebruikt in de integratie. Het ontvangt de voorraadniveauwaarden uit Finance and Operations tijdens de integratie en transformeert die waarden vervolgens in journalen voor handmatige voorraad waarmee vervolgens de voorraadproducten in het magazijn worden gewijzigd. 

## <a name="prerequisites-and-mapping-setup"></a>Vereisten en instellingen voor toewijzing

### <a name="in-the-data-integration-project"></a>In het project Gegevensintegratie
Pas filters toe met Geavanceerde query en filtering om in te stellen dat alleen voorraadniveaugegevens voor de gewenste producten en magazijnen vanuit Finance and Operations naar Field Service worden verzonden.

## <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

### <a name="product-inventory-finance-and-operations-to-field-service-product-inventory"></a>Productvoorraad (Finance and Operations naar Field Service): Productvoorraad

[![Sjabloontoewijzing in Gegevensintegratie](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)

