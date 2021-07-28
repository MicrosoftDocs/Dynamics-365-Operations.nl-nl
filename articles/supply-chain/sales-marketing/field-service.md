---
title: Overzicht van integratie met Microsoft Dynamics 365 Field Service
description: In dit onderwerp vindt u een overzicht van de integratie met Microsoft Dynamics 365 Field Service.
author: ChristianRytt
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 2ceb95198332d6a9da057d657771fe6fcca5c5b9
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 07/06/2021
ms.locfileid: "6359600"
---
# <a name="integration-with-microsoft-dynamics-365-field-service-overview"></a>Overzicht van integratie met Microsoft Dynamics 365 Field Service

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Supply Chain Management maakt synchronisatie van zakelijke processen mogelijk tussen Dynamics 365 Supply Chain Management en Dynamics 365 Field Service. De integratiescenario's worden geconfigureerd met uitbreidbare Gegevensintegrator-sjablonen en de Microsoft Dataverse voor het inschakelen van de synchronisatie van bedrijfsprocessen.
Standaardsjablonen kunnen worden gebruikt om aangepaste integratieprojecten te maken waarin extra standaard en aangepaste kolommen en tabellen kunnen worden toegewezen voor het corrigeren van de integratie en om aan specifieke zakelijke behoeften te voldoen. 

De Field Service-integratie borduurt voort op de bestaande functionaliteit voor prospect tot contant geld.

![Synchronisatie van zakelijke processen tussen Supply Chain Management en Field Service.](./media/field-service-integration.png)

De eerste fase van de integratie tussen Field Service en Supply Chain Management is gericht op het inschakelen van werkorders en overeenkomsten in het Field Service dien worden gefactureerd in Supply Chain Management. De ondersteunde stroom begint in Field Service, waar informatie uit werkorders wordt gesynchroniseerd met Supply Chain Management als verkooporders. In Supply Chain Management worden de verkooporders gefactureerd om factuurdocumenten te genereren. Bovendien wordt de informatie van overeenkomstfacturen in Field Service gesynchroniseerd met Supply Chain Management. De Microsoft Dynamics 365 Gegevensintegrator synchroniseert gegevens met behulp van aanpasbare projecten. Standaardsjablonen kunnen worden gebruikt om aangepaste integratieprojecten te maken waarin extra standaard en aangepaste kolommen en ook tabellen kunnen worden toegewezen voor het corrigeren van de integratie en voor het voldoen aan specifieke behoeften.

In de eerste fase van de integratie tussen Field Service en Supply Chain Management wordt de synchronisatie gestart van de volgende items:

- [Producten in Supply Chain Management synchroniseren met producten in Field Service](field-service-product.md)
- [Werkorders in Field Service synchroniseren met verkooporders in Supply Chain Management](field-service-work-order.md)
- [Overeenkomstfacturen in Field Service synchroniseren met vrije-tekstfacturen in Supply Chain Management](field-service-invoice.md)

Bekijk de korte YouTube-video om een voorbeeld te zien van hoe u een werkorder synchroniseert tussen Field Service en Supply Chain Management: [Een werkorder synchroniseren met Integratie van Microsoft Dynamics 365](https://www.youtube.com/watch?v=46ylO7raZAo).

## <a name="integration-with-field-service-including-inventory-and-project-information"></a>Integratie met Field Service, met inbegrip van voorraad- en projectgegevens

De aanvullende functionaliteit in deze tweede fase is erop gericht om technici inzicht in de voorraadgegevens uit Supply Chain Management te bieden zodat zij voorraadniveaus kunnen bijwerken en materiaal kunnen overboeken. Daarnaast profiteren bedrijven die verkochte goederen installeren of onderhouden van betere controle over en zichtbaarheid in het volledige verkoop- en serviceproces met de integratie van projecten.

### <a name="functionality-includes-integration-of"></a>Functionaliteit omvat de integratie van:
- Magazijngegevens
- Informatie over voorhanden voorraad
- Voorraadoverboekingen
- Voorraadcorrecties
- Supply Chain Management-projecten die zijn verbonden met Dynamics 365 Field Service-werkorders
- Dynamics 365 Field Service-werkorders met koppeling naar Supply Chain Management-projecten passen dit projectnummer op de verkooporder toe om facturering van het project toe te staan. 

![Synchronisatie van zakelijke processen tussen Supply Chain Management en Field Service.](./media/FSv2overview.png)

### <a name="the-second-phase-of-the-integration-between-field-service-and-supply-chain-management-enables-synchronization-with-the-following-templates"></a>In de tweede fase van de integratie tussen Field Service en Supply Chain Management wordt de synchronisatie met de volgende sjablonen ingeschakeld:
- Magazijnen (Supply Chain Management naar Field Service) - Magazijnen van Supply Chain Management naar Field Service [Geavanceerde query] 
- Productvoorraad (Supply Chain Management naar Field Service) - Voorraadniveaugegevens van Supply Chain Management naar Field Service [Geavanceerde query] 
- Voorraadcorrectie (Field Service naar Supply Chain Management) - Voorraadcorrecties van Field Service naar Supply Chain Management [Geavanceerde query] 
- Voorraadoverboekingen (Field Service naar Supply Chain Management) - Voorraadoverboekingen van Field Service naar Supply Chain Management [Geavanceerde query] 
- Projecten (Supply Chain Management naar Field Service) - Projectlijst van Supply Chain Management naar Field Service 
- Werkorders met Project (Field Service naar Supply Chain Management) - Werkorders in Field Service naar verkooporders in Supply Chain Management, met ondersteuning voor Project [Geavanceerde query] 
- Field Service-producten met Voorraadeenheid (Supply Chain Management naar Sales) - 'Verkoopbare vrijgegeven producten' in Supply Chain Management naar 'Producten' in Sales voor Field Service, inclusief Voorraadeenheid 

## <a name="system-requirements"></a>Systeemvereisten

### <a name="system-requirements-for-supply-chain-management"></a>Systeemvereisten voor Supply Chain Management
Field Service-integratie ondersteunt de volgende versies:

- Dynamics 365 for Finance and Operations versie 8.1.2 (december 2018) is uitgebracht in december 2018 en heeft een toepassingsbuildnummer 8.1.195 met Platform update 22 (7.0.5095). 

### <a name="system-requirements-for-field-service"></a>Systeemvereisten voor Field Service
Als u de oplossing Field Service-integratie wilt gebruiken, moet u de volgende onderdelen installeren:

- Field Service (versie 8.2.0.286) of een latere versie van Dynamics 365 9.1.x - uitgebracht in november 2018
- De oplossing Prospect naar contant geld (P2C) voor Dynamics 365, versie 1.15.0.1 of een hogere versie. De oplossing kan worden gedownload van [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
- De oplossing Field Service-integratie, -project en -voorraad voor Dynamics 365, versie 2.0.0.0 of een hogere versie. De oplossing kan worden gedownload van [AppSource](https://appsource.microsoft.com/product/dynamics-365/mscrm.p2cfieldserviceintegrationv2).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]