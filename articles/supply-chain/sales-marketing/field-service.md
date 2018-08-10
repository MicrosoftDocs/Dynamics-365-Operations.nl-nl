---
title: Integratie met Microsoft Dynamics 365 for Field Service
description: In dit onderwerp vindt u een overzicht van de integratie met Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: a57e23691a6b4d48c6b8dd6d1f61fc9730365b39
ms.openlocfilehash: 0c1268d2fddcf7b28ecfc3197f21e9d30a5a5855
ms.contentlocale: nl-nl
ms.lasthandoff: 05/31/2018

---


# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a>Integratie met Microsoft Dynamics 365 for Field Service

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations maakt synchronisatie mogelijk van bedrijfsprocessen tussen Finance and Operations en Microsoft Dynamics 365 for Field Service. De integratiescenario's worden geconfigureerd met uitbreidbare Gegevensintegrator-sjablonen en de Common Data Service (CDS) voor het inschakelen van de synchronisatie van bedrijfsprocessen.

[![Synchronisatie van zakelijke processen tussen Finance and Operations en Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)

De eerste fase van de integratie tussen Field Service en Finance and Operations is gericht op het inschakelen van werkorders en overeenkomsten in het Field Service dien worden gefactureerd in Finance and Operations. De ondersteunde stroom begint in Field Service, waar informatie uit werkorders wordt gesynchroniseerd met Finance and Operations als verkooporders. In Finance and Operations worden de verkooporders gefactureerd voor het genereren van factuurdocumenten. Bovendien wordt de informatie van overeenkomstfacturen in Field Service gesynchroniseerd met Finance and Operations. De Microsoft Dynamics 365 Gegevensintegrator synchroniseert gegevens met behulp van aanpasbare projecten. Standaardsjablonen kunnen worden gebruikt om aangepaste integratieprojecten te maken waarin extra standaardvelden en aangepaste velden en entiteiten kunnen worden toegewezen voor het corrigeren van de integratie en voor het voldoen aan specifieke behoeften.

In de eerste fase van de integratie tussen Field Service en Finance and Operations wordt de synchronisatie gestart van de volgende items:

- [Producten in Finance and Operations met producten van Field Service die informatie over het producttype bevatten](field-service-product.md)
- [Werkorders in Field Service met verkooporders in Finance and Operations](field-service-work-order.md)
- [Facturen in Field Service vrije-tekstfacturen in Finance and Operations](field-service-invoice.md)

Bekijk de korte YouTube-video om een voorbeeld te zien van hoe u een werkorder synchroniseert tussen Field Service en Finance and Operations, [Een werkorder synchroniseren tussen Dynamics 365 for Field Service en Finance and Operations](https://www.youtube.com/watch?v=hAB4TDVMjxU).

[![](https://img.youtube.com/vi/hAB4TDVMjxU/0.jpg)](https://www.youtube.com/watch?v=hAB4TDVMjxU)

## <a name="system-requirements-for-finance-and-operations"></a>Systeemvereisten voor Finance and Operations
Field Service-integratie ondersteunt de volgende versies:

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a>Dynamics 365 for Finance and Operations versie 8.0 (April 2018) of later

- Dynamics 365 for Finance and Operations versie 8.0 (April 2018) is uitgebracht in april 2018 en heeft een buildnummer 8.0.30.8020 met Platform Update 15 (7.0.4841.35234). 

## <a name="system-requirements-for-field-service"></a>Systeemvereisten voor Field Service
Als u de oplossing Field Service-integratie wilt gebruiken, moet u de volgende onderdelen installeren:

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a>Microsoft Dynamics 365 for Field Service 9.0 of hoger

- Dynamics 365 for Field Service-versie 1612 (9.0.1.733) (DB 9.0.1.733) online of een hogere versie.
- De oplossing Prospect naar contant geld (P2C) voor Dynamics 365, versie 1.15.0.1 of een hogere versie. De oplossing kan worden gedownload van [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- De oplossing Field Service-integratie voor Dynamics 365, versie 1.0.0.0 of een hogere versie. De oplossing kan worden gedownload van [AppSource](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.p2cfieldserviceintegration).

