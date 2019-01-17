---
title: Integratie met Microsoft Dynamics 365 for Field Service
description: In dit onderwerp vindt u een overzicht van de integratie met Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 08/25/2018
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
ms.sourcegitcommit: 95031534c43dc0578e258bc3e5376c429d72b0ab
ms.openlocfilehash: 673ab2a101cee1a3dbbb1249f582d959cecc7f7f
ms.contentlocale: nl-nl
ms.lasthandoff: 12/23/2018

---

# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a>Integratie met Microsoft Dynamics 365 for Field Service

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations maakt synchronisatie mogelijk van bedrijfsprocessen tussen Finance and Operations en Microsoft Dynamics 365 for Field Service. De integratiescenario's worden geconfigureerd met uitbreidbare Gegevensintegrator-sjablonen en de Common Data Service (CDS) voor het inschakelen van de synchronisatie van bedrijfsprocessen.
Standaardsjablonen kunnen worden gebruikt om aangepaste integratieprojecten te maken waarin extra standaardvelden en aangepaste velden en entiteiten kunnen worden toegewezen voor het corrigeren van de integratie en om aan specifieke zakelijke behoeften te voldoen. 

De Field Service-integratie borduurt voort op de bestaande functionaliteit voor prospect tot contant geld.

![Synchronisatie van zakelijke processen tussen Finance and Operations en Field Service](./media/field-service-integration.png)

De eerste fase van de integratie tussen Field Service en Finance and Operations is gericht op het inschakelen van werkorders en overeenkomsten in het Field Service dien worden gefactureerd in Finance and Operations. De ondersteunde stroom begint in Field Service, waar informatie uit werkorders wordt gesynchroniseerd met Finance and Operations als verkooporders. In Finance and Operations worden de verkooporders gefactureerd voor het genereren van factuurdocumenten. Bovendien wordt de informatie van overeenkomstfacturen in Field Service gesynchroniseerd met Finance and Operations. De Microsoft Dynamics 365 Gegevensintegrator synchroniseert gegevens met behulp van aanpasbare projecten. Standaardsjablonen kunnen worden gebruikt om aangepaste integratieprojecten te maken waarin extra standaardvelden en aangepaste velden en entiteiten kunnen worden toegewezen voor het corrigeren van de integratie en voor het voldoen aan specifieke behoeften.

In de eerste fase van de integratie tussen Field Service en Finance and Operations wordt de synchronisatie gestart van de volgende items:

- [Producten in Finance and Operations met producten van Field Service die informatie over het producttype bevatten](field-service-product.md)
- [Werkorders in Field Service met verkooporders in Finance and Operations](field-service-work-order.md)
- [Facturen in Field Service vrije-tekstfacturen in Finance and Operations](field-service-invoice.md)

Bekijk de korte YouTube-video om een voorbeeld te zien van hoe u een werkorder synchroniseert tussen Field Service en Finance and Operations, [Een werkorder synchroniseren met Integratie van Microsoft Dynamics 365](https://www.youtube.com/watch?v=46ylO7raZAo).

## <a name="system-requirements-for-finance-and-operations"></a>Systeemvereisten voor Finance and Operations
Field Service-integratie ondersteunt de volgende versies:

### <a name="dynamics-365-for-finance-and-operations-version-80-april-2018-or-later"></a>Dynamics 365 for Finance and Operations versie 8.0 (April 2018) of later

- Dynamics 365 for Finance and Operations versie 8.0 (April 2018) is uitgebracht in april 2018 en heeft een buildnummer 8.0.30.8020 met Platform Update 15 (7.0.4841.35234). 

## <a name="system-requirements-for-field-service"></a>Systeemvereisten voor Field Service
Als u de oplossing Field Service-integratie wilt gebruiken, moet u de volgende onderdelen installeren:

### <a name="microsoft-dynamics-365-for-field-service-90-or-later"></a>Microsoft Dynamics 365 for Field Service 9.0 of hoger

- Dynamics 365 for Field Service-versie 1612 (9.0.1.733) (DB 9.0.1.733) online of een hogere versie.
- De oplossing Prospect naar contant geld (P2C) voor Dynamics 365, versie 1.15.0.1 of een hogere versie. De oplossing kan worden gedownload van [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- De oplossing Field Service-integratie voor Dynamics 365, versie 1.0.0.0 of een hogere versie. De oplossing kan worden gedownload van [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegration).

# <a name="integration-with-microsoft-dynamics-365-for-field-service-including-inventory-and-project-information"></a>Integratie met Microsoft Dynamics 365 for Field Service, inclusief voorraad- en projectgegevens

De aanvullende functionaliteit in deze tweede fase is erop gericht om technici inzicht in de voorraadgegevens uit Finance and Operations te bieden zodat zij voorraadniveaus kunnen bijwerken en materiaal kunnen overboeken. Daarnaast profiteren bedrijven die verkochte goederen installeren of onderhouden van betere controle over en zichtbaarheid in het volledige verkoop- en serviceproces met de integratie van projecten.

### <a name="functionality-includes-integration-of"></a>Functionaliteit omvat de integratie van:
- Magazijngegevens
- Informatie over voorhanden voorraad
- Voorraadoverboekingen
- Voorraadcorrecties
- Dynamics 365 for Finance and Operations-projecten verbonden met Dynamics 365 for Field Service-werkorders
- Dynamics 365 for Field Service-werkorders met een koppeling naar Dynamics 365 for Finance and Operations-projects, pas dit projectnummer toe aan de Dynamics 365 for Finance and Operations-verkooporder om vanuit het project te kunnen factureren. 

![Synchronisatie van zakelijke processen tussen Finance and Operations en Field Service](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-finance-and-operations-enables-synchronization-with-the-following-templates"></a>In de tweede fase van de integratie tussen Field Service en Finance and Operations wordt de synchronisatie met de volgende sjablonen ingeschakeld:
- Magazijnen (Fin and Ops naar Field Service) - Magazijnen vanuit Finance and Operations naar Field Service [Geavanceerde query] 
- Productvoorraad (Fin and Ops naar Field Service) - Voorraadniveaugegevens vanuit Finance and Operations naar Field Service [Geavanceerde query] 
- Voorraadcorrectie (Field Service naar Fin and Ops) - Voorraadcorrecties vanuit Field Service naar Finance and Operations [Geavanceerde query] 
- Voorraadoverboekingen (Field Service naar Fin and Ops) - Voorraadoverboekingen vanuit Field Service naar Finance and Operations [Geavanceerde query] 
- Projecten (Fin and Ops naar Field Service) - Projectlijst vanuit Finance and Operations naar Field Service 
- Werkorders met Project (Field Service naar Fin and Ops) - Werkorders in Field Service naar verkooporders in Finance and Operations, met ondersteuning voor Project [Geavanceerde query] 
- Field Service-producten met Voorraadeenheid (Fin and Ops naar Sales) - 'Verkoopbare vrijgegeven producten' in Finance and Operations naar 'Producten' in Sales voor Field Service, inclusief Voorraadeenheid 

## <a name="system-requirements-for-finance-and-operations"></a>Systeemvereisten voor Finance and Operations
Field Service-integratie ondersteunt de volgende versies:

- Dynamics 365 for Finance and Operations versie 8.1.2 (december 2019) is uitgebracht in december 2019 en heeft een buildnummer 8.1.195 met platformupdate 22 (7.0.5095). 

## <a name="system-requirements-for-field-service"></a>Systeemvereisten voor Field Service
Als u de oplossing Field Service-integratie wilt gebruiken, moet u de volgende onderdelen installeren:

- Field Service for Dynamics 365 (versie 8.2.0.286) of een latere versie van Dynamics 365 9.1.x - Uitgebracht in november 2018
- De oplossing Prospect naar contant geld (P2C) voor Dynamics 365, versie 1.15.0.1 of een hogere versie. De oplossing kan worden gedownload van [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- De oplossing Field Service-integratie, -project en -voorraad voor Dynamics 365, versie 2.0.0.0 of een hogere versie. De oplossing kan worden gedownload van [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).

