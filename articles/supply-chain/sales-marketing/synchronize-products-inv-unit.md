---
title: Producten met voorraadeenheid uit Supply Chain Management synchroniseren met Field Service
description: Dit artikel bespreekt de sjablonen en de onderliggende taak die worden gebruikt om producten met voorraadeenheid te synchroniseren van Dynamics 365 Supply Chain Management naar Dynamics 365 Field Service.
author: Henrikan
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: henrikan
ms.dyn365.ops.version: 8.1.3
ms.search.validFrom: 2018-12-01
ms.openlocfilehash: 5f7658eacd20aa69a64d6288e9d29e53b6ccb002
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8887249"
---
# <a name="synchronize-products-with-inventory-unit-from-supply-chain-management-to-field-service"></a>Producten met voorraadeenheid uit Supply Chain Management synchroniseren met Field Service

[!include[banner](../includes/banner.md)]

Dit artikel bespreekt de sjablonen en de onderliggende taak die worden gebruikt om producten met voorraadeenheid te synchroniseren van Dynamics 365 Supply Chain Management naar Dynamics 365 Field Service.

[![Synchronisatie van zakelijke processen tussen Supply Chain Management en Field Service.](./media/FSProductsOW.png)](./media/FSProductsOW.png)

De gebruikte sjabloon **Field Service-producten met Voorraadeenheid (Supply Chain Management naar Field Service)** is gebaseerd op de sjabloon **Field Service-producten (Supply Chain Management naar Field Service)**. Zie voor meer informatie [Producten in Supply Chain Management synchroniseren met producten in Field Service](field-service-product.md).

In dit artikel worden alleen de verschillen tussen de twee sjablonen beschreven: 
- **Field Service-producten met Voorraadeenheid (Supply Chain Management naar Service)**
- **Field Service-producten (Supply Chain Management naar Field Service)** 

## <a name="templates-and-tasks"></a>Sjablonen en taken

**Naam van de sjabloon in Gegevensintegratie:**

- Field Service-producten met Voorraadeenheid (Supply Chain Management naar Service)

**Naam van de taak in het project Gegevensintegratie:**

- Producten

De gebruikte sjabloon **Field Service-producten met Voorraadeenheid (Supply Chain Management naar Field Service)** omvat een toewijzing die niet is inbegrepen in de sjabloon **Field Service-producten (Supply Chain Management naar Field Service)**. Deze toewijzing zorgt ervoor dat de voorraadeenheid die nodig is voor synchronisatie op voorraadniveau wordt opgenomen.

```plaintext
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

In de volgende afbeeldingen ziet u de sjabloontoewijzing in Gegevensintegratie.

### <a name="field-service-products-with-inventory-unit-supply-chain-management-to-field-service-products"></a>Field Service-producten met Voorraadeenheid (Supply Chain Management naar Field Service): Products

[![Sjabloontoewijzing in Gegevensintegratie.](./media/FSProduct1.png)](./media/FSProduct1.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]