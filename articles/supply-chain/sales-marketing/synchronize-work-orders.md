---
title: Werkorders met project vanuit Field Service synchroniseren naar Finance and Operations
description: Dit onderwerp bespreekt de sjablonen en de onderliggende taak die worden gebruikt om werkorders met een projectnummer te synchroniseren van Microsoft Dynamics 365 for Field Service naar Microsoft Dynamics 365 for Finance and Operations.
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
ms.openlocfilehash: 5ca01b085315d916a18c512af28fc7534ce76ee8
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/07/2019
ms.locfileid: "1536728"
---
# <a name="synchronize-work-orders-with-project-from-field-service-to-finance-and-operations"></a>Werkorders met project vanuit Field Service synchroniseren naar Finance and Operations

[!include[banner](../includes/banner.md)]

Dit onderwerp bespreekt de sjablonen en de onderliggende taak die worden gebruikt om werkorders met een projectnummer te synchroniseren van Microsoft Dynamics 365 for Field Service naar Microsoft Dynamics 365 for Finance and Operations.

[![Synchronisatie van zakelijke processen tussen Finance and Operations en Field Service](./media/FSSOprojectOW.png)](./media/FSSOprojectOW.png)

De gebruikte sjabloon **Werkorders met project (Field Service met Fin and Ops)** is gebaseerd op de sjabloon **Werkorders (Field Service met Fin and Ops)**. Zie voor meer informatie [Werkorders in Field Service synchroniseren met verkooporders in Finance and Operations](https://docs.microsoft.com/en-us/dynamics365/unified-operations/supply-chain/sales-marketing/field-service-work-order).

In dit onderwerp worden alleen de verschillen tussen de twee sjablonen beschreven:
- **Werkorders met project (Field Service met Finance and Operations)**
- **Werkorders (Field Service met Finance and Operations)**

Het belangrijkste verschil is dat deze sjabloon toewijzing van het projectnummer toegewezen aan de werkorder in Field Service omvat, zodat de verkooporder gemaakt in Finance and Operations het projectnummer bevat en dat de facturering in het gerelateerde project kan worden uitgevoerd. Daarnaast worden de functies voor geavanceerde query's en filters gebruikt.

## <a name="templates-and-tasks"></a>Sjablonen en taken

**Naam van de sjabloon in Gegevensintegratie:**

- Werkorders met project (Field Service met Finance and Operations)

**Naam van de taak in het project Gegevensintegratie:**

- WorkOrderHeader
- WorkOrderHeaderProject
- WorkOrderProduct
- WorkOrderService

## <a name="field-service-crm-solution"></a>Field Service CRM-oplossing
Het veld **Extern project** is toegevoegd aan de entiteit Werkorder. Dit veld is een opzoekveld en wanneer u uw werkorder aan een project koppelt, wordt de verkooporder verbonden met een project in Finance and Operations. Zodra de **systeemstatus** van Geopend of In uitvoering in een hogere status wordt gewijzigd, wordt het veld **Extern project** vergrendeld en kunt u de waarde niet toevoegen, verwijderen of wijzigen.

## <a name="template-mapping-in-data-integration"></a>Sjabloontoewijzing in Gegevensintegratie

In de volgende afbeeldingen ziet u de sjabloontoewijzing in Gegevensintegratie.

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheader"></a>Werkorders met project (Field Service met Finance and Operations): WorkOrderHeader

[![Sjabloontoewijzing in Gegevensintegratie](./media/FSWOP1.png)](./media/FSWOP1.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderheaderproject"></a>Werkorders met project (Field Service met Finance and Operations): WorkOrderHeaderProject

[![Sjabloontoewijzing in Gegevensintegratie](./media/FSWOP2.png)](./media/FSWOP2.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderproduct"></a>Werkorders met project (Field Service met Finance and Operations): WorkOrderProduct

[![Sjabloontoewijzing in Gegevensintegratie](./media/FSWOP3.png)](./media/FSWOP3.png)

### <a name="work-orders-with-project-field-service-to-fin-and-ops-workorderservice"></a>Werkorders met project (Field Service met Finance and Operations): WorkOrderService

[![Sjabloontoewijzing in Gegevensintegratie](./media/FSWOP4.png)](./media/FSWOP4.png)
