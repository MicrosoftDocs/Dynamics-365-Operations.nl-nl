---
title: Werkorders synchroniseren met projecten van Field Service Supply Chain Management
description: Dit artikel bespreekt de sjablonen en de onderliggende taak die worden gebruikt om werkorders met een projectnummer te synchroniseren van Dynamics 365 Field Service naar Dynamics 365 Supply Chain Management.
author: Henrikan
ms.date: 03/12/2019
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
ms.openlocfilehash: a43a7f7e900205bdb23fb9a35ca1518369683a42
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860488"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-supply-chain-management"></a>Werkorders synchroniseren met projecten van Field Service Supply Chain Management

[!include[banner](../includes/banner.md)]

Dit artikel bespreekt de sjablonen en de onderliggende taak die worden gebruikt om werkorders met een projectnummer te synchroniseren van Dynamics 365 Field Service naar Dynamics 365 Supply Chain Management.

[![Synchronisatie van zakelijke processen tussen Supply Chain Management en Field Service.](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

De gebruikte sjabloon **Werkorders met Project (Field Service naar Supply Chain Management)** is gebaseerd op de sjabloon **Werkorders (Field Service naar Supply Chain Management)**. Zie voor meer informatie [Werkorders in Field Service synchroniseren met verkooporders in Supply Chain Management](/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

In dit artikel worden alleen de verschillen tussen de twee sjablonen beschreven:
- **Werkorders met Project (Field Service naar Supply Chain Management)**
- **Werkorders (Field Service naar Supply Chain Management)**

Het belangrijkste verschil is dat deze sjabloon toewijzing van het projectnummer omvat dat in Field Service aan de werkorder is toegewezen, zodat de Verkooporder die in Supply Chain Management is gemaakt, het projectnummer bevat en dat de facturering in het gerelateerde project kan worden uitgevoerd. Daarnaast worden de functies voor geavanceerde query's en filters gebruikt.

## <a name="templates-and-tasks"></a>Sjablonen en taken

**Naam van de sjabloon in Gegevensintegratie:**

- Werkorders met Project (Field Service naar Supply Chain Management)

**Naam van de taak in het project Gegevensintegratie:**

- WorkOrderHeader
- WorkOrderHeaderProject
- WorkOrderProduct
- WorkOrderService

## <a name="field-service-crm-solution"></a>Field Service CRM-oplossing
Het veld **Extern project** is toegevoegd aan de entiteit Werkorder. Dit veld is een opzoekveld en wanneer u uw Werkorder aan een project koppelt, wordt de Verkooporder verbonden met een project in Supply Chain Management. Zodra de **Systeemstatus** van Geopend – In uitvoering(690,970,000) in een hogere status wordt gewijzigd, wordt het veld **Extern project** vergrendeld en kunt u de waarde niet toevoegen, verwijderen of wijzigen.

## <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

In de volgende afbeeldingen ziet u de sjabloontoewijzing in Gegevensintegratie.

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheader"></a>Werkorders met Project (Field Service naar Supply Chain Management): WorkOrderHeader

[![Sjabloontoewijzing in Gegevensintegratie, Werkorders met Project (Field Service naar Supply Chain Management): WorkOrderHeader.](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderheaderproject"></a>Werkorders met Project (Field Service naar Supply Chain Management): WorkOrderHeaderProject

[![Sjabloontoewijzing in Gegevensintegratie, Werkorders met Project (Field Service naar Supply Chain Management): WorkOrderHeaderProject.](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderproduct"></a>Werkorders met Project (Field Service naar Supply Chain Management): WorkOrderProduct

[![Sjabloontoewijzing in Gegevensintegratie, Werkorders met Project (Field Service naar Supply Chain Management): WorkOrderProduct.](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-supply-chain-management-workorderservice"></a>Werkorders met Project (Field Service naar Supply Chain Management): WorkOrderService

[![Sjabloontoewijzing in Gegevensintegratie, Werkorders met Project (Field Service naar Supply Chain Management): WorkOrderService.](./media/FSWOP4.png)](./media/FSWOP4.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]