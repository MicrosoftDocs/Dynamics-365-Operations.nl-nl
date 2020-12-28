---
title: Prospect naar contant geld
description: Dit onderwerp bevat een overzicht van de oplossing Prospect naar contant geld tussen Dynamics 365 Supply Chain Management en Dynamics 365 Sales.
author: ChristianRytt
manager: tfehr
ms.date: 04/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 55c39fac40498488519fcb539b3c3f7560a46b30
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4425371"
---
# <a name="prospect-to-cash"></a>Van prospect naar contant geld

[!include [banner](../includes/banner.md)]

De oplossing Prospect naar contant geld biedt directe synchronisatie tussen Dynamics 365 Supply Chain Management en Dynamics 365 Sales. De Prospect naar contant geld-sjablonen die beschikbaar zijn in de functie Gegevensintegratie activeren de stroom van gegevens voor rekeningen, contactpersonen, producten, verkoopoffertes en verkoopfacturen. Terwijl de gegevens worden verplaatst, kunt u verkoop- en marketingactiviteiten uitvoeren in Sales en de orderafhandeling verwerken met voorraadbeheer in Supply Chain Management. 

Bekijk de korte YouTube-video voor meer informatie over de integratie van Integratie van prospect naar contant geld: [Integratie van prospect naar contant geld](https://www.youtube.com/watch?v=AVV9x5x-XCg).

In de huidige versie biedt de oplossing Prospect naar contant geld de volgende typen directe synchronisatie:

- [Rekeningen rechtstreeks vanuit Sales synchroniseren met klanten in Supply Chain Management](accounts-template-mapping-direct.md)
- [Producten rechtstreeks vanuit Supply Chain Management synchroniseren met producten in Sales](products-template-mapping-direct.md)
- [Contactpersonen in Sales rechtstreeks synchroniseren met contactpersonen of klanten in Supply Chain Management](contacts-template-mapping-direct.md)
- [Kopteksten en regels in verkoopoffertes rechtstreeks synchroniseren vanuit Sales naar Supply Chain Management](sales-quotation-template-mapping-sales-fin.md)
- [Verkooporders rechtstreeks tussen Sales en Supply Chain Management synchroniseren](sales-order-template-mapping-direct-two-ways.md)
- [Kopteksten en regels in verkoopfacturen rechtstreeks synchroniseren vanuit Supply Chain Management naar Sales](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-supply-chain-management"></a>Systeemvereisten voor Supply Chain Management
Integratie van Prospect met contant geld wordt ondersteund door de volgende versies:

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a>Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (december 2017)

- Dynamics 365 for Finance and Operations, Enterprise edition (december 2017) - toepassingsbuild 7.3.11971.56116 met Platform Update 12 (7.0.4709.41129)

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a>Dynamics 365 for Finance and Operations, Enterprise edition (juli 2017)

- Dynamics 365 for Finance and Operations, Enterprise edition (juli 2017) - met Platform Update 8 (toepassingsbuild 7.2.11792.56024 met platformbuild 7.0.4565.16212).
- De volgende hotfixes zijn vereist:

  - **[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)**: deze hotfix maakt synchronisatie van verkooporders vanuit Sales met Supply Chain Management mogelijk via de functie Gegevensintegratie. Daarnaast bevat de hotfix diverse andere verbeteringen.
  - **[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)**: deze hotfix maakt synchronisatie van verkooporderregels vanuit Supply Chain Management naar Sales mogelijk via de functie Gegevensintegratie.
  - **[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)**: deze hotfix maakt synchronisatie van verkooporders vanuit Supply Chain Management met Sales mogelijk via de functie Gegevensintegratie.

    > [!NOTE]
    > U hoeft alleen KB4045570 te installeren omdat de installatie de wijzigingen van andere hotfixes bevat. 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a>Dynamics 365 for Finance and Operations versie 1611 (november 2016)

- Dynamics 365 for Finance and Operations versie 1611 (november 2016) met Platform Update 8 of hoger

- De volgende hotfixes zijn vereist:

  - **[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)**: De synchronisatie van verkooporders met Gegevensintegrator van Supply Chain Management naar Sales inschakelen. 
  - **[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)**: De synchronisatie van verkooporderkoppen en -regels met Gegevensintegrator van Supply Chain Management naar Sales inschakelen.
  - **[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)**: Ondersteuning voor de integratie van Prospect naar contant geld via gegevensentiteiten is vereist.
    
    > [!NOTE]
    > Na installatie van de hotfixes moet u de volgende batchtaak triggeren vanuit het formulier **SalesPopulateProspectToCash**. Dit formulier is verborgen omdat u het maar eenmaal nodig hebt. U opent het formulier door u aan te melden bij de omgeving en het volgende aan de URL in uw browseradres toe te voegen: *&mi=action:SalesPopulateProspectToCash*, bijvoorbeeld `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`. Wanneer het formulier wordt geopend, klikt u op OK. In de tabellen **SalesLine**, **SalesQuotationLine** en **CustInvoiceTrans** wordt een nieuw veld **LineCreationSequnceNumber** gevuld met unieke waarden en de lijst met producten wordt vernieuwd. Dit is nodig voor een geslaagde integratie van Prospect naar contant geld.


## <a name="system-requirements-for-sales"></a>Systeemvereisten voor Sales

Als u de oplossing Prospect naar contant geld wilt gebruiken, moet u de volgende onderdelen installeren:

- Dynamics 365 Sales-versie 1612 (8.2.1.207) (DB 8.2.1.207) online of een hogere versie.
- De oplossing Prospect naar contant geld voor Dynamics 365 Sales, versie 1.15.0.0 of een hogere versie. De oplossing kan worden gedownload van AppSource. [Download Dynamics 365, Prospect naar contant geld](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).
