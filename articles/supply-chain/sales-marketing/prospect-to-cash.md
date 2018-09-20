---
title: Prospect naar contant geld
description: Dit onderwerp biedt een overzicht van de oplossing Prospect naar contant geld tussen Microsoft Dynamics 365 for Finance and Operations en Microsoft Dynamics 365 for Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, SalesTable, EcoResProductListPage
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
ms.sourcegitcommit: ce9c24a0a89dd4e6a0f3f2c7789b4f553d88d412
ms.openlocfilehash: b46ece384a28f8e78989253fcf467fbf3feaf1b7
ms.contentlocale: nl-nl
ms.lasthandoff: 08/13/2018

---

# <a name="prospect-to-cash"></a>Prospect naar contant geld

[!include [banner](../includes/banner.md)]

De oplossing Prospect naar contant geld biedt directe synchronisatie tussen Dynamics 365 for Finance and Operations en Dynamics 365 for Sales. De Prospect naar contant geld-sjablonen die beschikbaar zijn in de functie Gegevensintegratie activeren de stroom van gegevens voor rekeningen, contactpersonen, producten, verkoopoffertes en verkoopfacturen tussen Finance and Operations en Sales. Terwijl de gegevens tussen Finance and Operations en Sales worden verplaatst, kunt u verkoop- en marketingactiviteiten uitvoeren in Sales en de orderafhandeling verwerken met voorraadbeheer in Finance and Operations. 

Bekijk de korte YouTube-video voor meer informatie over de integratie van Prospect met contant geld: [Integratie van Prospect met contant geld](https://www.youtube.com/watch?v=AVV9x5x-XCg).

In de huidige versie biedt de oplossing Prospect naar contant geld de volgende typen directe synchronisatie:

- [Rekeningen in Sales onderhouden en direct vanuit Sales naar Finance and Operations synchroniseren](accounts-template-mapping-direct.md)
- [Producten in Finance and Operations onderhouden en direct synchroniseren met Sales](products-template-mapping-direct.md)
- [Contactpersonen in Sales onderhouden en direct synchroniseren met contactpersonen of klanten in Finance and Operations](contacts-template-mapping-direct.md)
- [Verkoopoffertes vanuit Sales rechtstreeks synchroniseren met Finance and Operations](sales-quotation-template-mapping-sales-fin.md)
- [Verkooporders rechtstreeks synchroniseren tussen Sales en Finance and Operations](sales-order-template-mapping-direct-two-ways.md)
- [Verkoopfacturen vanuit Finance and Operations rechtstreeks synchroniseren met Sales](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-finance-and-operations"></a>Systeemvereisten voor Finance and Operations
Integratie van Prospect met contant geld wordt ondersteund door de volgende versies:

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a>Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 (december 2017)

- Dynamics 365 for Finance and Operations, Enterprise Edition (december 2017) - toepassingsbuild 7.3.11971.56116 met platformupdate 12 (7.0.4709.41129)

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a>Dynamics 365 for Finance and Operations, Enterprise-editie (juli 2017)

- Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017) - met platformupdate 8 (toepassingsbuild 7.2.11792.56024 met platformbuild 7.0.4565.16212).
- De volgende hotfixes zijn vereist:

  - **[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)**: met deze hotfix kunnen verkooporders met de functie Gegevensintegratie van Sales naar Finance and Operations worden gesynchroniseerd. Daarnaast bevat de hotfix diverse andere verbeteringen.
  - **[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)**: met deze hotfix kunnen verkooporderregels met de functie Gegevensintegratie van Finance and Operations naar Sales worden gesynchroniseerd.
  - **[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)**: met deze hotfix kunnen verkooporders met de functie Gegevensintegratie van Finance and Operations naar Sales worden gesynchroniseerd.

    > [!NOTE]
    > U hoeft alleen KB4045570 te installeren omdat de installatie de wijzigingen van andere hotfixes bevat. 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a>Versie 1611 van Dynamics 365 for Finance and Operations (november 2016)

- Versie 1611 van Dynamics 365 for Finance and Operations (november 2016) met platformupdate 8 of hoger

- De volgende hotfixes zijn vereist:

  - **[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)**: De synchronisatie van verkooporders met Gegevensintegrator van Finance and Operations naar Sales inschakelen. 
  - **[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)**: De synchronisatie van kopteksten en regels van verkooporders met Gegevensintegrator van Finance and Operations naar Sales inschakelen.
  - **[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)**: Ondersteuning voor de integratie van Prospect naar contant geld via gegevensentiteiten is vereist.
    
    > [!NOTE]
    > Na installatie van de hotfixes moet u de volgende batchtaak triggeren vanuit het formulier **SalesPopulateProspectToCash**. Dit formulier is verborgen omdat u het maar eenmaal nodig hebt. U opent het formulier door u aan te melden bij de omgeving en het volgende aan de URL in uw browseradres toe te voegen: *&mi=action:SalesPopulateProspectToCash*, bijvoorbeeld `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`. Wanneer het formulier wordt geopend, klikt u op OK. In de tabellen **SalesLine**, **SalesQuotationLine** en **CustInvoiceTrans** wordt een nieuw veld **LineCreationSequnceNumber** gevuld met unieke waarden en de lijst met producten wordt vernieuwd. Dit is nodig voor een geslaagde integratie van Prospect naar contant geld.


## <a name="system-requirements-for-sales"></a>Systeemvereisten voor Sales

Als u de oplossing Prospect naar contant geld wilt gebruiken, moet u de volgende onderdelen installeren:

- Dynamics 365 for Sales-versie 1612 (8.2.1.207) (DB 8.2.1.207) online of een hogere versie.
- De oplossing Prospect naar contant geld voor Dynamics 365 for Sales, versie 1.15.0.0 of hoger. De oplossing kan worden gedownload van AppSource. [Download Dynamics 365, Prospect naar contant geld](https://appsource.microsoft.com/en-us/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).

