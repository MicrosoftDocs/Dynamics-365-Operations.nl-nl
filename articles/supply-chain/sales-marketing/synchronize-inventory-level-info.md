---
title: Voorraadcorrecties uit Supply Chain Management synchroniseren met Field Service
description: Dit onderwerp bespreekt de sjablonen en de onderliggende taken die worden gebruikt om informatie op voorraadniveau te synchroniseren van Dynamics 365 Supply Chain Management naar Dynamics 365 Field Service.
author: ChristianRytt
manager: tfehr
ms.date: 05/07/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 0822bf4bdbb687e040e2ce04842ef263b8dc0e1a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243076"
---
# <a name="synchronize-inventory-level-information-from-supply-chain-management-to-field-service"></a>Voorraadcorrecties uit Supply Chain Management synchroniseren met Field Service 

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dit onderwerp bespreekt de sjablonen en de onderliggende taken die worden gebruikt om informatie op voorraadniveau te synchroniseren van Dynamics 365 Supply Chain Management naar Dynamics 365 Field Service.

[![Synchronisatie van zakelijke processen tussen Supply Chain Management en Field Service](./media/FSOnHandOW.png)](./media/FSOnHandOW.png)

## <a name="templates-and-tasks"></a>Sjablonen en taken
De volgende sjabloon en onderliggende taken worden gebruikt voor het synchroniseren van grijpvoorraadniveaus vanuit Supply Chain Management naar Field Service.

**Sjabloontoewijzing in Gegevensintegratie**
- Productvoorraad (Supply Chain Management naar Field Service)
  
**Taak in het project Gegevensintegratie**
- Productvoorraad

De volgende synchronisatietaken moeten worden uitgevoerd voordat de synchronisatie van voorraadniveaus kan plaatsvinden:
- Magazijnen (Supply Chain Management naar Field Service) 
- Field Service-producten met Voorraadeenheid (Supply Chain Management naar Sales) 

## <a name="entity-set"></a>Entiteitset

| Field Service                      | Supply Chain Management                |
|------------------------------------|----------------------------------------|
| msdynce_externalproductinventories | Voorhanden Dataverse-voorraad per magazijn     |

## <a name="entity-flow"></a>Entiteitstroom
Voorraadniveaugegevens worden vanuit Finance and Operations naar Field Service verzonden voor geselecteerde producten. Voorraadniveaugegevens bevatten: 
- Voorhanden hoeveelheid (huidige geregistreerde fysieke hoeveelheid in het magazijn)
- Hoeveelheid in bestelling (totale geregistreerde hoeveelheid in bestelling, zoals verkooporders)
- Bestelde hoeveelheid (totale geregistreerde bestelde hoeveelheid, zoals inkooporders)

Deze gegevens worden per vrijgegeven product geregistreerd voor elk magazijn en gesynchroniseerd op basis van wijzigingstracering wanneer het voorraadniveau verandert.

In Field Service worden met de integratieoplossing voorraadjournalen voor de delta gemaakt om ervoor te zorgen dat de niveaus in Field Service overeenkomen met de niveaus in Supply Chain Management.

Supply Chain Management fungeert als master voor voorraadniveaus. Daarom is het belangrijk om de integratie voor werkorders, overboekingen en correcties van Field Service naar Supply Chain Management in te stellen als deze functionaliteit wordt gebruikt in Field Service. Daarnaast moeten voorraadniveaus vanuit Supply Chain Management worden gesynchroniseerd.

De producten en magazijnen waarvoor voorraadniveaus worden gemaakt via Supply Chain Management kunnen worden beheerd met Geavanceerde query's en filters (Power Query).

> [!NOTE]
> Het is mogelijk om meerdere magazijnen in Field Services te maken (met **Wordt extern beheerd = Nee**) en deze toe te wijzen aan één magazijn in Supply Chain Management met de functies voor Geavanceerde query's en filters. Dit wordt gebruikt in situaties waarin u wilt dat Field Service het gedetailleerde voorraadniveau beheert en alleen updates verzendt naar Supply Chain Management. In dit geval ontvangt Field Service geen updates over voorraadniveaus van Supply Chain Management. Zie voor meer informatie [Voorraadcorrecties vanuit Field Service synchroniseren naar Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/synchronize-inventory-adjustments) en [Werkorders in Field Service synchroniseren met verkooporders in Supply Chain Management](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

## <a name="field-service-crm-solution"></a>Field Service CRM-oplossing
De entiteit **Externe productvoorraad** is een nieuwe entiteit die alleen voor de back-end wordt gebruikt in de integratie. Deze entiteit ontvangt de voorraadniveauwaarden uit Supply Chain Management tijdens de integratie en transformeert die waarden vervolgens in Journalen voor handmatige voorraad waarmee vervolgens de voorraadproducten in het Magazijn worden gewijzigd.

## <a name="prerequisites-and-mapping-setup"></a>Vereisten en instellingen voor toewijzing

### <a name="data-integration"></a>Gegevensintegratie
Het project werkt alleen als u ervoor zorgt dat de integratiesleutel wordt bijgewerkt voor msdynce_externalproductinventories.
1.  Ga naar **Gegevensintegratie > Verbindingssets**.
2.  Selecteer de gebruikte verbindingsset.
3.  Controleer op het tabblad **Integratiesleutel** of de volgende sleutels aan msdynce_externalproductinventories zijn toegevoegd:
      - msdynce_productnumber (productnummer)
      - msdynce_warehouseid (magazijn-id)
      
### <a name="data-integration-project"></a>Gegevensintegratieproject
U kunt filters toepassen met Geavanceerde query´s en filters, zodat dat alleen bepaalde producten en magazijnen informatie over het voorraadniveau vanuit Supply Chain Management naar Field Service worden verzonden.

## <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

### <a name="product-inventory-supply-chain-management-to-field-service-product-inventory"></a>Productvoorraad (Supply Chain Management naar Field Service): Productvoorraad

[![Sjabloontoewijzing in Gegevensintegratie](./media/FSinventoryLevel1.png)](./media/FSinventoryLevel1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]