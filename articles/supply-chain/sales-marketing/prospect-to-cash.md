---
title: Prospect naar contant geld
description: Het onderwerp biedt een overzicht van de oplossing Prospect naar contant geld tussen Dynamics 365 for Finance and Operations, Enterprise edition en Dynamics 365 for Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
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
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 674d2e1f2c5cdbccf43618a9083ca01abed0735a
ms.openlocfilehash: 2accf77c5241adff7ad1648737dde451153fde46
ms.contentlocale: nl-nl
ms.lasthandoff: 11/14/2017

---

# <a name="prospect-to-cash"></a>Prospect naar contant geld  

[!include[banner](../includes/banner.md)]

De oplossing Prospect naar contant geld gebruikt [Gegevensintegratie](/common-data-service/entity-reference/dynamics-365-integration) om gegevens te synchroniseren tussen exemplaren van Microsoft Dynamics 365 for Finance and Operations, Enterprise edition en Dynamics 365 for Sales via Common Data Service (CDS). De Prospect naar contant geld-sjablonen in de functie Gegevensintegratie activeren de stroom van gegevens over rekeningen, contactpersoon, producten, verkoopoffertes en verkoopfacturen tussen Finance and Operations en Sales. Terwijl de gegevens tussen Finance and Operations en Sales worden verplaatst, kunt u verkoop- en marketingactiviteiten uitvoeren in Sales en de orderafhandeling verwerken met voorraadbeheer in Finance and Operations. 

Deze oplossing biedt integratie in de volgende gebieden: 

-   [Rekeningen in Sales onderhouden en ze synchroniseren met Finance and Operations](accounts-template-mapping.md)
-   [Contactpersonen in Sales onderhouden en ze synchroniseren met Finance and Operations](contacts-template-mapping.md)
-   [Producten in Finance and Operations onderhouden en ze synchroniseren met Sales](products-template-mapping.md)
-   [Verkoopoffertes maken in Sales en ze synchroniseren met Finance and Operations](sales-quotation-template-mapping.md)
-   [Verkooporders maken in Finance and Operations en ze synchroniseren met Sales](sales-order-template-mapping.md)
-   [Verkoopfacturen maken in Finance and Operations en ze synchroniseren met Sales](sales-invoice-template-mapping.md)

Deze oplossing biedt directe synchronisatie in de volgende gebieden:

-   [Rekeningen in Sales onderhouden en direct vanuit Sales naar Finance and Operations synchroniseren](accounts-template-mapping-direct.md)
-   [Producten in Finance and Operations onderhouden en direct synchroniseren naar Sales](products-template-mapping-direct.md)
-   [Contactpersonen in Sales onderhouden en direct synchroniseren naar contactpersonen of klanten in Finance and Operations](contacts-template-mapping-direct.md)
-   [Kopteksten en regels in verkoopoffertes vanuit Sales direct synchroniseren naar Finance and Operations](sales-quotation-template-mapping-sales-fin.md)
-   [Verkooporders maken in Finance and Operations en direct synchroniseren naar Sales](sales-order-template-mapping-direct.md)
-  [Kopteksten en regels in verkooporders direct synchroniseren tussen Sales en Finance and Operations](sales-order-template-mapping-between-sales-fin.md)
-   [Verkooporders direct synchroniseren tussen Sales en Finance and Operations](sales-order-template-mapping-direct-two-ways.md)
-   [Verkoopfacturen maken in Finance and Operations en direct synchroniseren naar Sales](sales-invoice-template-mapping-direct.md)


## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a>Systeemvereisten voor Dynamics 365 for Finance and Operations, Enterprise edition

Als u de oplossing Prospect naar contant geld wilt gebruiken, moet u het volgende installeren:

- Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (juli 2017) met platformupdate 8 (App 7.2.11792.56024 met platform 7.0.4565.16212)

- Hotfixes voor Dynamics 365 for Finance and Operations, Enterprise edition (juli 2017).
        
    -  [KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160) - Deze hotfix biedt naast een aantal andere verbeteringen ondersteuning voor het synchroniseren van verkooporders vanuit Sales naar Finance and Operations met de functie Gegevensintegratie.

    -  [KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2): met deze hotfix kunnen verkooporderregels met de functie Gegevensintegratie van Finance and Operations met Sales worden gesynchroniseerd.
        
    -  [KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2): met deze hotfix kunnen verkooporders met de functie Gegevensintegratie van Finance and Operations met Sales worden gesynchroniseerd.

**Opmerking**: u hoeft alleen KB4045570 te installeren omdat de installatie de wijzigingen van de andere KB's bevat.
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a>Systeemvereisten voor Dynamics 365 for Sales

Als u de oplossing Prospect naar contant geld wilt gebruiken, moet u het volgende installeren:

- Dynamics 365 for Sales-versie 1612 (8.2.1.207) (DB 8.2.1.207) online.
- De oplossing Prospect naar contant geld voor Dynamics 365 for Sales, versie 1.14.0.0 (v14) of hoger.

### <a name="install-the-prospect-to-cash-solution-for-sales"></a>De oplossing Prospect naar contant geld voor Sales installeren

- Download het [zipbestand met de oplossing Prospect naar contant geld voor Dynamics 365 for Sales](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) op CustomerSource.

- Zorg ervoor dat het zipbestand niet wordt geblokkeerd om te voorkomen dat het foutbericht Er zijn geen importpakketten gevonden wordt weergegeven wanneer u het oplossingspakket installeert. Ga als volgt te werk om de blokkering van het bestand op te heffen:

    -  Klik met de rechtermuisknop op het zipbestand.
    -  Selecteer **Eigenschappen** en selecteer vervolgens **Deblokkeren**. 

- Pak het zipbestand uit en voer PackageDeployer.exe uit.

- Installeer de oplossing Prospect naar contant geld in uw exemplaar van Sales.

    - Selecteer het implementatietype **Office 365**.
    - Selecteer **Geavanceerd weergeven**.
    - Selecteer een **regio** voor een snelle installatie. Als u **Geen idee** selecteert, worden alle regio's gezocht en duurt de installatie langer.
    - Voer de **gebruikersnaam** en het **wachtwoord** voor een beheerder in die over de gebruikersrechten beschikt om te installeren.

