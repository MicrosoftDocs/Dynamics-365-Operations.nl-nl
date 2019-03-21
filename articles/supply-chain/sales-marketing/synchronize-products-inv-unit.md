---
title: Producten met voorraadeenheid uit Finance and Operations synchroniseren met Field Service
description: Dit onderwerp bespreekt de sjablonen en de onderliggende taak die worden gebruikt om producten met voorraadeenheid te synchroniseren van Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 03/12/2019
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
ms.openlocfilehash: 8e421be79fde6103be6344040b6ae6cda0626c5a
ms.sourcegitcommit: d9ed934a142b88340d268fd2bd3753475a3712b0
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/12/2019
ms.locfileid: "836297"
---
# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a>Producten met voorraadeenheid uit Finance and Operations synchroniseren met Field Service

[!include[banner](../includes/banner.md)]

Dit onderwerp bespreekt de sjablonen en de onderliggende taak die worden gebruikt om producten met voorraadeenheid te synchroniseren van Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service.

[![Synchronisatie van zakelijke processen tussen Finance and Operations en Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)

De gebruikte sjabloon **Field Service-producten met Voorraadeenheid (Finance and Operations met Field Service)** is gebaseerd op de sjabloon **Field Service-producten (Finance and Operations met Field Service)**. Zie voor meer informatie [Field Service-producten (Finance and Operations met Field Service)](field-service-product.md).

In dit onderwerp worden alleen de verschillen tussen de twee sjablonen beschreven: 
- **Field Service-producten met Voorraadeenheid (Finance and Operations naar Sales)**
- **Field Service-producten (Finance and Operations met Field Service)** 

## <a name="templates-and-tasks"></a>Sjablonen en taken

**Naam van de sjabloon in Gegevensintegratie:**

- Field Service-producten met Voorraadeenheid (Finance and Operations naar Sales)

**Naam van de taak in het project Gegevensintegratie:**

- Producten

De sjabloon **Field Service-producten met Voorraadeenheid (Finance and Operations naar Field Service)** bevat één toewijzing die niet is opgenomen in de sjabloon **Field Service-producten (Finance and Operations naar Field Service)**. Deze toewijzing zorgt ervoor dat de voorraadeenheid die nodig is voor synchronisatie op voorraadniveau wordt opgenomen.

```
INVENTORYUNITSYMBOL [INVENTORYUNITSYMBOL]         Fn        msdynce_inventoryunit.name [Inventory Unit(Name)] 
```

## <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

In de volgende afbeeldingen ziet u de sjabloontoewijzing in Gegevensintegratie.

### <a name="field-service-products-with-inventory-unit-finance-and-operations-to-field-service-products"></a>Field Service-producten met Voorraadeenheid (Finance and Operations naar Field Service): Producten

[![Sjabloontoewijzing in Gegevensintegratie](./media/FSProduct1.png)](./media/FSProduct1.png)
