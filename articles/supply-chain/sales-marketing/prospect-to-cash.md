---
title: Prospect naar contant geld
description: Dit onderwerp biedt een overzicht van de oplossing Prospect naar contant geld tussen Microsoft Dynamics 365 for Finance and Operations, Enterprise edition en Microsoft Dynamics 365 for Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 11/17/2017
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
ms.sourcegitcommit: 788e64476094e84eb4d438890776306c05b20582
ms.openlocfilehash: 762699cf68ec8a9df5db20d7dd33bc9248f0a36e
ms.contentlocale: nl-nl
ms.lasthandoff: 12/11/2017

---

# <a name="prospect-to-cash"></a>Prospect naar contant geld

[!include[banner](../includes/banner.md)]

De oplossing Prospect naar contant geld biedt directe synchronisatie tussen Microsoft Dynamics 365 for Finance and Operations, Enterprise edition en Microsoft Dynamics 365 for Sales. De Prospect naar contant geld-sjablonen die beschikbaar zijn in de functie Gegevensintegratie activeren de stroom van gegevens voor rekeningen, contactpersonen, producten, verkoopoffertes en verkoopfacturen tussen Finance and Operations en Sales. Terwijl de gegevens tussen Finance and Operations en Sales worden verplaatst, kunt u verkoop- en marketingactiviteiten uitvoeren in Sales en de orderafhandeling verwerken met voorraadbeheer in Finance and Operations.

In de huidige versie biedt de oplossing Prospect naar contant geld de volgende typen directe synchronisatie:

- [Rekeningen in Sales onderhouden en direct vanuit Sales naar Finance and Operations synchroniseren](accounts-template-mapping-direct.md)
- [Producten in Finance and Operations onderhouden en direct synchroniseren naar Sales](products-template-mapping-direct.md)
- [Contactpersonen in Sales onderhouden en direct synchroniseren naar contactpersonen of klanten in Finance and Operations](contacts-template-mapping-direct.md)
- [Verkoopoffertes direct vanuit Sales synchroniseren naar Finance and Operations](sales-quotation-template-mapping-sales-fin.md)
- [Verkooporders direct vanuit Finance and Operations synchroniseren naar Sales](sales-order-template-mapping-direct.md)
- [Verkooporders direct synchroniseren tussen Sales en Finance and Operations](sales-order-template-mapping-direct-two-ways.md)
- [Verkoopofferte direct vanuit Finance and Operations synchroniseren naar Sales](sales-invoice-template-mapping-direct.md)

In eerdere versies biedt de oplossing Prospect naar contant geld de volgende typen niet-directe synchronisatie:

- [Rekeningen in Sales onderhouden en ze synchroniseren met Finance and Operations](accounts-template-mapping.md)
- [Contactpersonen in Sales onderhouden en ze synchroniseren met Finance and Operations](contacts-template-mapping.md)
- [Producten in Finance and Operations onderhouden en ze synchroniseren met Sales](products-template-mapping.md)
- [Verkoopoffertes maken in Sales en ze synchroniseren met Finance and Operations](sales-quotation-template-mapping.md)
- [Verkooporders maken in Finance and Operations en ze synchroniseren met Sales](sales-order-template-mapping.md)
- [Verkoopfacturen maken in Finance and Operations en ze synchroniseren met Sales](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-finance-and-operations"></a>Systeemvereisten voor Finance and Operations

Als u de oplossing Prospect naar contant geld wilt gebruiken, moet u de volgende onderdelen installeren:

### <a name="july-2017"></a>Juli 2017 

- Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (juli 2017) met platformupdate 8 (toepassingsbuild 7.2.11792.56024 met platformbuild 7.0.4565.16212)
- De volgende hotfixes voor Finance and Operations:

    - **[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)**: met deze hotfix kunnen verkooporders met de functie Gegevensintegratie van Sales naar Finance and Operations worden gesynchroniseerd. Daarnaast bevat de hotfix diverse andere verbeteringen.
    - **[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)**: met deze hotfix kunnen verkooporderregels met de functie Gegevensintegratie van Finance and Operations naar Sales worden gesynchroniseerd.
    - **[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)**: met deze hotfix kunnen verkooporders met de functie Gegevensintegratie van Finance and Operations naar Sales worden gesynchroniseerd.

    > [!NOTE]
    > U hoeft alleen KB4045570 te installeren omdat de installatie de wijzigingen van de andere KB-artikelen (Microsoft Knowledge Base) bevat.

### <a name="november-2016-version-1611"></a>November 2016 (versie 1611)

- Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (november 2016) met platformupdate 8 of hoger

- De volgende hotfixes voor Finance and Operations:

    - **[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)**: De synchronisatie van verkooporders met Gegevensintegrator van Microsoft Dynamics 365 for Finance and Operations naar Sales inschakelen 
    - **[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)**: De synchronisatie van kopteksten en regels van verkooporders met Gegevensintegrator van Microsoft Dynamics 365 for Finance and Operations naar Sales inschakelen
    - **[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)**: Ondersteuning voor de integratie van Prospect naar contant geld via gegevensentiteiten is vereist
    
    > [!NOTE]
    > Na installatie van de hotfixes moet u de volgende batchtaak triggeren vanuit het formulier SalesPopulateProspectToCash. Dit formulier is verborgen omdat u het maar eenmaal nodig hebt. U opent het formulier door het volgende aan uw browseradres toe te voegen wanneer u bent aangemeld bij de omgeving: &mi=action:SalesPopulateProspectToCash: https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash. Klik in het formulier dat wordt geopend op OK.
    In de tabellen SalesLine, SalesQuotationLine en CustInvoiceTrans wordt een nieuw veld LineCreationSequnceNumber gevuld met unieke waarden en de lijst met producten wordt vernieuwd. Dit is nodig om de P2C-integratie te laten werken in 7.1


## <a name="system-requirements-for-sales"></a>Systeemvereisten voor Sales

Als u de oplossing Prospect naar contant geld wilt gebruiken, moet u de volgende onderdelen installeren:

- Microsoft Dynamics 365 for Sales-versie 1612 (8.2.1.207) (DB 8.2.1.207) online
- De oplossing Prospect naar contant geld voor Microsoft Dynamics 365 for Sales, versie 1.15.0.0 (v15) 

   > [!NOTE]
   >
   > Sjablonen met versie 1.0.0.0 en 1.0.0.1 worden ondersteund in de oplossing Prospect naar contant geld voor Microsoft Dynamics 365 for Sales, versie 1.14.1.0
   >
   > Sjablonen met versie 2.0.0.0 en 2.1.0.0 worden ondersteund in de oplossing Prospect naar contant geld voor Microsoft Dynamics 365 for Sales, versie 1.15.0.0

### <a name="install-the-prospect-to-cash-solution-for-sales"></a>De oplossing Prospect naar contant geld voor Sales installeren

1. Download het [zipbestand met de oplossing Prospect naar contant geld voor Dynamics 365 for Sales](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) van CustomerSource.
2. Zorg ervoor dat het zipbestand niet wordt geblokkeerd. Anders wordt het foutbericht Er zijn geen importpakketten gevonden weergegeven wanneer u het oplossingspakket installeert. Als u het zipbestand wilt deblokkeren, klikt u er met de rechtermuisknop op en selecteert u **Eigenschappen**. Selecteer vervolgens **Deblokkeren**.
3. Pak het zipbestand uit en voer **PackageDeployer.exe** uit.
4. Installeer de oplossing Prospect naar contant geld in uw exemplaar van Sales:

    1. Selecteer **Office 365** als het implementatietype.
    2. Selecteer **Geavanceerd weergeven**.
    3. Selecteer een regio voor een snelle installatie. Als u **Geen idee** selecteert, worden alle regio's gezocht en duurt de installatie langer.
    4. Voer de gebruikersnaam en het wachtwoord in voor een beheerder die over installatierechten beschikt.

