---
title: Integratie met Microsoft Dynamics 365 for Field Service
description: In dit onderwerp vindt u een overzicht van de integratie met Microsoft Dynamics 365 for Field Service.
author: ChristianRytt
manager: AnnBe
ms.date: 02/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: efda4e39f63155785386ecec6d21973e01a0f69f
ms.sourcegitcommit: 704d273485dcdc25c97a222bc0ef0695aad334d2
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/28/2019
ms.locfileid: "770888"
---
# <a name="integration-with-microsoft-dynamics-365-for-field-service"></a>Integratie met Microsoft Dynamics 365 for Field Service

[!include[banner](../includes/banner.md)]

Microsoft Dynamics 365 for Finance and Operations maakt synchronisatie van zakelijke processen tussen Finance and Operations en Microsoft Dynamics 365 for Field Service mogelijk. De integratiescenario's worden geconfigureerd met uitbreidbare Gegevensintegrator-sjablonen en de Common Data Service (CDS) voor het inschakelen van de synchronisatie van bedrijfsprocessen.
Standaardsjablonen kunnen worden gebruikt om aangepaste integratieprojecten te maken waarin extra standaardvelden en aangepaste velden en entiteiten kunnen worden toegewezen voor het corrigeren van de integratie en om aan specifieke zakelijke behoeften te voldoen. 

De Field Service-integratie borduurt voort op de bestaande functionaliteit voor prospect tot contant geld.

![Synchronisatie van zakelijke processen tussen Finance and Operations en Field Service](./media/field-service-integration.png)

De eerste fase van de integratie tussen Field Service en Finance and Operations is gericht op het inschakelen van werkorders en overeenkomsten in het Field Service dien worden gefactureerd in Finance and Operations. De ondersteunde stroom begint in Field Service, waar informatie uit werkorders wordt gesynchroniseerd met Finance and Operations als verkooporders. In Finance and Operations worden de verkooporders gefactureerd voor het genereren van factuurdocumenten. Bovendien wordt de informatie van overeenkomstfacturen in Field Service gesynchroniseerd met Finance and Operations. De Microsoft Dynamics 365 Gegevensintegrator synchroniseert gegevens met behulp van aanpasbare projecten. Standaardsjablonen kunnen worden gebruikt om aangepaste integratieprojecten te maken waarin extra standaardvelden en aangepaste velden en entiteiten kunnen worden toegewezen voor het corrigeren van de integratie en voor het voldoen aan specifieke behoeften.

In de eerste fase van de integratie tussen Field Service en Finance and Operations wordt de synchronisatie gestart van de volgende items:

- [Producten in Finance and Operations met producten van Field Service die informatie over het producttype bevatten](field-service-product.md)
- [Werkorders in Field Service met verkooporders in Finance and Operations](field-service-work-order.md)
- [Facturen in Field Service vrije-tekstfacturen in Finance and Operations](field-service-invoice.md)

Bekijk de korte YouTube-video om een voorbeeld te zien van hoe u een werkorder synchroniseert tussen Field Service en Finance and Operations: [Een werkorder synchroniseren met Integratie van Microsoft Dynamics 365](https://www.youtube.com/watch?v=46ylO7raZAo).

## <a name="integration-with-microsoft-dynamics-365-for-field-service-including-inventory-and-project-information"></a>Integratie met Microsoft Dynamics 365 for Field Service, met inbegrip van voorraad- en projectgegevens

De aanvullende functionaliteit in deze tweede fase is erop gericht om technici inzicht in de voorraadgegevens uit Finance and Operations te bieden zodat zij voorraadniveaus kunnen bijwerken en materiaal kunnen overboeken. Daarnaast profiteren bedrijven die verkochte goederen installeren of onderhouden van betere controle over en zichtbaarheid in het volledige verkoop- en serviceproces met de integratie van projecten.

### <a name="functionality-includes-integration-of"></a>Functionaliteit omvat de integratie van:
- Magazijngegevens
- Informatie over voorhanden voorraad
- Voorraadoverboekingen
- Voorraadcorrecties
- Dynamics 365 for Finance and Operations-projecten die zijn verbonden met Dynamics 365 for Field Service-werkorders
- Dynamics 365 for Field Service-werkorders met koppeling naar Dynamics 365 for Finance and Operations-projecten passen dit projectnummer op de Dynamics 365 for Finance and Operations-verkooporder toe om facturering van het project toe te staan. 

![Synchronisatie van zakelijke processen tussen Finance and Operations en Field Service](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-finance-and-operations-enables-synchronization-with-the-following-templates"></a>In de tweede fase van de integratie tussen Field Service en Finance and Operations wordt de synchronisatie met de volgende sjablonen ingeschakeld:
- Magazijnen (Fin and Ops naar Field Service) - Magazijnen vanuit Finance and Operations naar Field Service [Geavanceerde query] 
- Productvoorraad (Fin and Ops naar Field Service) - Voorraadniveaugegevens vanuit Finance and Operations naar Field Service [Geavanceerde query] 
- Voorraadcorrectie (Field Service naar Fin and Ops) - Voorraadcorrecties vanuit Field Service naar Finance and Operations [Geavanceerde query] 
- Voorraadoverboekingen (Field Service naar Fin and Ops) - Voorraadoverboekingen vanuit Field Service naar Finance and Operations [Geavanceerde query] 
- Projecten (Fin and Ops naar Field Service) - Projectlijst vanuit Finance and Operations naar Field Service 
- Werkorders met Project (Field Service naar Fin and Ops) - Werkorders in Field Service naar verkooporders in Finance and Operations, met ondersteuning voor Project [Geavanceerde query] 
- Field Service-producten met Voorraadeenheid (Fin and Ops naar Sales) - 'Verkoopbare vrijgegeven producten' in Finance and Operations naar 'Producten' in Sales voor Field Service, inclusief Voorraadeenheid 

## <a name="system-requirements"></a>Systeemvereisten

### <a name="system-requirements-for-finance-and-operations"></a>Systeemvereisten voor Finance and Operations
Field Service-integratie ondersteunt de volgende versies:

- Dynamics 365 for Finance and Operations versie 8.1.2 (december 2018) is uitgebracht in december 2018 en heeft een toepassingsbuildnummer 8.1.195 met Platform Update 22 (7.0.5095). 

### <a name="system-requirements-for-field-service"></a>Systeemvereisten voor Field Service
Als u de oplossing Field Service-integratie wilt gebruiken, moet u de volgende onderdelen installeren:

- Field Service for Dynamics 365 (versie 8.2.0.286) of een latere versie van Dynamics 365 9.1.x - uitgebracht in november 2018
- De oplossing Prospect naar contant geld (P2C) voor Dynamics 365, versie 1.15.0.1 of een hogere versie. De oplossing kan worden gedownload van [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- De oplossing Field Service-integratie, -project en -voorraad voor Dynamics 365, versie 2.0.0.0 of een hogere versie. De oplossing kan worden gedownload van [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).
