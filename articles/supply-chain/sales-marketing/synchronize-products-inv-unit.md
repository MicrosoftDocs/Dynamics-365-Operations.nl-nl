---
title: Producten met voorraadeenheid uit Finance and Operations synchroniseren met Field Service
description: In dit onderwerp komen de sjablonen en onderliggende taak aan de orde voor het synchroniseren van producten met een voorraadeenheid vanuit Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service.
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
ms.openlocfilehash: 5d3767c1a499f3d888d8fc2ce06c2837442e39f0
ms.contentlocale: nl-nl
ms.lasthandoff: 12/20/2018

---

# <a name="synchronize-products-with-inventory-unit-from-finance-and-operations-to-field-service"></a>Producten met voorraadeenheid uit Finance and Operations synchroniseren met Field Service

[!include[banner](../includes/banner.md)]

In dit onderwerp komen de sjablonen en onderliggende taak aan de orde voor het synchroniseren van producten met een voorraadeenheid vanuit Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service.

[![Synchronisatie van zakelijke processen tussen Finance and Operations en Field Service](./media/FSProductsOW.png)](./media/FSProductsOW.png)

De gebruikte sjabloon **Field Service-producten (Finance and Operations naar Field Service)** is gebaseerd op de sjabloon **Producten (Finance and Operations naar Sales) - Direct** van Prospect naar contant geld. Zie voor meer informatie [Producten (Finance and Operations naar Sales) - Direct](products-template-mapping-direct.md).

In dit onderwerp worden alleen de verschillen beschreven tussen de sjablonen **Field Service-producten (Finance and Operations naar Field Service)** en **Field Service-producten (Finance and Operations naar Field Service)**.

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

