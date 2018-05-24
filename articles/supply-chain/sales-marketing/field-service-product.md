---
title: Producten van Finance and Operations synchroniseren met producten in Field Service
description: In dit onderwerp komen de sjablonen en onderliggende taak aan de orde voor het synchroniseren van producten vanuit Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: ace66c037953f4b1b2e8b93a315faefdb090b1eb
ms.openlocfilehash: bf5de13fee6db1b467c1cf4d5cc65b46c67b29fe
ms.contentlocale: nl-nl
ms.lasthandoff: 05/08/2018

---

# <a name="synchronize-products-in-finance-and-operations-to-products-in-field-service"></a>Producten van Finance and Operations synchroniseren met producten in Field Service

[!include[banner](../includes/banner.md)]

In dit onderwerp komen de sjablonen en onderliggende taak aan de orde voor het synchroniseren van producten vanuit Microsoft Dynamics 365 for Finance and Operations naar Microsoft Dynamics 365 for Field Service.

De gebruikte sjabloon **Field Service-producten (Fin and Ops naar Field Service)** is gebaseerd op de sjabloon **Producten (Fin and Ops naar Sales) - Direct** van Prospect naar contant geld. Zie voor meer informatie [Producten (Fin and Ops naar Sales) - Direct](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

In dit onderwerp worden alleen de verschillen beschreven tussen de sjablonen **Field Service-producten (Fin and Ops naar Field Service)** en **Producten (Fin and Ops naar Sales) - Direct**.

## <a name="templates-and-tasks"></a>Sjablonen en taken

**Naam van de sjabloon in Gegevensintegratie:**

- Field Service-producten (Fin and Ops naar Field Service)

**Naam van de taak in het project Gegevensintegratie:**

- Producten - Producten

De sjabloon **Field Service-producten (Fin and Ops naar Field Service)** omvat één toewijzing die niet is ogpenomen in sjabloon **Producten (Fin and Ops naar Sales) - Direct**. Deze toewijzing zorgt ervoor dat het vereiste Field Service-veld **Producttype Field Service** correct wordt ingesteld.

```
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

De volgende waardetoewijzing wordt gebruikt.

```
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

In Finance and Operations wordt de waarde **Producttype Field Service** in de gegevensentiteit **Verkoopbare vrijgegeven producten** als volgt berekend:

- **Voorraad:** producttype = product en Artikelmodelgroep, Product in voorraad = True
- **Niet-voorraad:** producttype = product en Artikelmodelgroep, Product in voorraad = False
- **Service:** Producttype = Service

## <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

In de volgende afbeeldingen ziet u de sjabloontoewijzing in Gegevensintegratie.

### <a name="field-service-products-fin-and-ops-to-field-service-products---products"></a>Field Service-producten (Fin en Ops aan Field Service): Producten - Producten

[![Sjabloontoewijzing in Gegevensintegratie](./media/FSProduct.png)](./media/FSProduct.png)

