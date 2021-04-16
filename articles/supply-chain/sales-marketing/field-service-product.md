---
title: Producten in Supply Chain Management synchroniseren met producten in Field Service
description: In dit onderwerp worden de sjablonen besproken en de onderliggende taak die wordt gebruikt om producten van Dynamics 365 Supply Chain Management te synchroniseren met Dynamics 365 Field Service.
author: ChristianRytt
ms.date: 04/09/2018
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
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 9cc8e93259119236093e02924d29df64dcc876bb
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810889"
---
# <a name="synchronize-products-in-supply-chain-management-to-products-in-field-service"></a>Producten in Supply Chain Management synchroniseren met producten in Field Service

[!include[banner](../includes/banner.md)]

Dit onderwerp bespreekt de sjablonen en onderliggende taak die worden gebruikt om producten te synchroniseren van Dynamics 365 Supply Chain Management naar Dynamics 365 Field Service.

De gebruikte sjabloon **Field Service-producten (Supply Chain Management naar Field Service)** is gebaseerd op de sjabloon **Producten (Supply Chain Management naar Sales) - Direct** van Prospect naar Contant geld. Zie voor meer informatie [Producten (Supply Chain Management naar Sales) - Direct](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/sales-marketing/products-template-mapping-direct).

In dit onderwerp worden alleen de verschillen beschreven tussen de sjablonen **Field Service-producten (Supply Chain Management naar Field Service)** en **Producten (Supply Chain Management naar Sales) - Direct**.

## <a name="templates-and-tasks"></a>Sjablonen en taken

**Naam van de sjabloon in Gegevensintegratie**

- Field Service-producten (Supply Chain Management naar Field Service)

**Naam van de taak in het project Gegevensintegratie**

- Producten - Producten

De gebruikte sjabloon **Field Service-producten (Supply Chain Management naar Field Service)** bevat één toewijzing die niet is inbegrepen in de sjabloon **Producten (Supply Chain Management naar Sales) - Direct**. Deze toewijzing zorgt ervoor dat het vereiste Field Service-veld **Producttype Field Service** correct wordt ingesteld.

```plaintext
FIELDSERVICEPRODUCTTYPE        Fn        msdyn_fieldserciveproducttype
```

De volgende waardetoewijzing wordt gebruikt.

```plaintext
inventory     :  690970000
nonInventory  :  690970001 
service       :  690970002 
```

In Supply Chain Management wordt de waarde **Producttype Field Service** in de gegevensentiteit **Verkoopbare vrijgegeven producten** als volgt berekend:

- **Voorraad:** producttype = product en Artikelmodelgroep, Product in voorraad = True
- **Niet-voorraad:** producttype = product en Artikelmodelgroep, Product in voorraad = False
- **Service:** Producttype = Service

## <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

In de volgende afbeeldingen ziet u de sjabloontoewijzing in Gegevensintegratie.

### <a name="field-service-products-supply-chain-management-to-field-service-products---products"></a>Field Service-producten (Supply Chain Management naar Field Service): Producten - Producten

[![Sjabloontoewijzing in Gegevensintegratie](./media/FSProduct.png)](./media/FSProduct.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]