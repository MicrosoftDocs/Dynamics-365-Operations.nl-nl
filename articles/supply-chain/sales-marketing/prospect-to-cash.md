---
title: Prospect naar contant geld
description: Dit onderwerp bevat een overzicht van de oplossing Prospect naar contant geld tussen Dynamics 365 Supply Chain Management en Dynamics 365 Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 04/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, SalesTable, EcoResProductListPage
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
ms.openlocfilehash: 1a96b7cfa57ec72b25f21d94fadb2fbf9bc6ea3b
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251347"
---
# <a name="prospect-to-cash"></a><span data-ttu-id="92a37-103">Van prospect naar contant geld</span><span class="sxs-lookup"><span data-stu-id="92a37-103">Prospect to cash</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="92a37-104">De oplossing Prospect naar contant geld biedt directe synchronisatie tussen Dynamics 365 Supply Chain Management en Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="92a37-104">The Prospect to cash solution provides direct synchronization across Dynamics 365 Supply Chain Management and Dynamics 365 Sales.</span></span> <span data-ttu-id="92a37-105">De Prospect naar contant geld-sjablonen die beschikbaar zijn in de functie Gegevensintegratie activeren de stroom van gegevens voor rekeningen, contactpersonen, producten, verkoopoffertes en verkoopfacturen.</span><span class="sxs-lookup"><span data-stu-id="92a37-105">The Prospect to cash templates that are available with the Data Integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices.</span></span> <span data-ttu-id="92a37-106">Terwijl de gegevens worden verplaatst, kunt u verkoop- en marketingactiviteiten uitvoeren in Sales en de orderafhandeling verwerken met voorraadbeheer in Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="92a37-106">While data is flowing, you can perform sales and marketing activities in Sales, and you can handle order fulfillment by using inventory management in Supply Chain Management.</span></span> 

<span data-ttu-id="92a37-107">Bekijk de korte YouTube-video voor meer informatie over de integratie van Integratie van prospect naar contant geld: [Integratie van prospect naar contant geld](https://www.youtube.com/watch?v=AVV9x5x-XCg).</span><span class="sxs-lookup"><span data-stu-id="92a37-107">For more information about the Prospect to cash integration, watch the short YouTube video [Prospect to cash integration](https://www.youtube.com/watch?v=AVV9x5x-XCg).</span></span>

<span data-ttu-id="92a37-108">In de huidige versie biedt de oplossing Prospect naar contant geld de volgende typen directe synchronisatie:</span><span class="sxs-lookup"><span data-stu-id="92a37-108">In the current version, the Prospect to cash solution provides the following types of direct synchronization:</span></span>

- [<span data-ttu-id="92a37-109">Rekeningen in Sales onderhouden en direct vanuit Sales naar Supply Chain Management synchroniseren</span><span class="sxs-lookup"><span data-stu-id="92a37-109">Maintain accounts in Sales and sync them directly from Sales to Supply Chain Management</span></span>](accounts-template-mapping-direct.md)
- [<span data-ttu-id="92a37-110">Producten in Supply Chain Management onderhouden en direct met Sales synchroniseren</span><span class="sxs-lookup"><span data-stu-id="92a37-110">Maintain products in Supply Chain Management and sync them directly to Sales</span></span>](products-template-mapping-direct.md)
- [<span data-ttu-id="92a37-111">Contactpersonen in Sales onderhouden en direct synchroniseren met contactpersonen of klanten in Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="92a37-111">Maintain contacts in Sales and sync them directly to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)
- [<span data-ttu-id="92a37-112">Verkoopoffertes rechtstreeks vanuit Sales synchroniseren met Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="92a37-112">Synchronize sales quotation directly from Sales to Supply Chain Management</span></span>](sales-quotation-template-mapping-sales-fin.md)
- [<span data-ttu-id="92a37-113">Verkooporders rechtstreeks tussen Sales en Supply Chain Management synchroniseren</span><span class="sxs-lookup"><span data-stu-id="92a37-113">Synchronize sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)
- [<span data-ttu-id="92a37-114">Verkoopfactuur rechtstreeks vanuit Supply Chain Management synchroniseren met Sales</span><span class="sxs-lookup"><span data-stu-id="92a37-114">Synchronize sales invoice directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-supply-chain-management"></a><span data-ttu-id="92a37-115">Systeemvereisten voor Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="92a37-115">System requirements for Supply Chain Management</span></span>
<span data-ttu-id="92a37-116">Integratie van Prospect met contant geld wordt ondersteund door de volgende versies:</span><span class="sxs-lookup"><span data-stu-id="92a37-116">Prospect to cash integration is supported on the following versions:</span></span>

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a><span data-ttu-id="92a37-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (december 2017)</span><span class="sxs-lookup"><span data-stu-id="92a37-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (December 2017)</span></span>

- <span data-ttu-id="92a37-118">Dynamics 365 for Finance and Operations, Enterprise edition (december 2017) - toepassingsbuild 7.3.11971.56116 met Platform Update 12 (7.0.4709.41129)</span><span class="sxs-lookup"><span data-stu-id="92a37-118">Dynamics 365 for Finance and Operations, Enterprise edition (December 2017) - Application build 7.3.11971.56116 with Platform Update 12 (7.0.4709.41129)</span></span>

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a><span data-ttu-id="92a37-119">Dynamics 365 for Finance and Operations, Enterprise edition (juli 2017)</span><span class="sxs-lookup"><span data-stu-id="92a37-119">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017)</span></span>

- <span data-ttu-id="92a37-120">Dynamics 365 for Finance and Operations, Enterprise edition (juli 2017) - met Platform Update 8 (toepassingsbuild 7.2.11792.56024 met platformbuild 7.0.4565.16212).</span><span class="sxs-lookup"><span data-stu-id="92a37-120">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) - with platform update 8 (application build 7.2.11792.56024 with platform build 7.0.4565.16212).</span></span>
- <span data-ttu-id="92a37-121">De volgende hotfixes zijn vereist:</span><span class="sxs-lookup"><span data-stu-id="92a37-121">The following hotfixes are required:</span></span>

  - <span data-ttu-id="92a37-122">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)**: deze hotfix maakt synchronisatie van verkooporders vanuit Sales met Supply Chain Management mogelijk via de functie Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="92a37-122">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – This hotfix enables sales order synchronization from Sales to Supply Chain Management via the Data Integration feature.</span></span> <span data-ttu-id="92a37-123">Daarnaast bevat de hotfix diverse andere verbeteringen.</span><span class="sxs-lookup"><span data-stu-id="92a37-123">It also provides several other enhancements.</span></span>
  - <span data-ttu-id="92a37-124">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)**: deze hotfix maakt synchronisatie van verkooporderregels vanuit Supply Chain Management naar Sales mogelijk via de functie Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="92a37-124">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order line synchronization from Supply Chain Management to Sales via the Data Integration feature.</span></span>
  - <span data-ttu-id="92a37-125">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)**: deze hotfix maakt synchronisatie van verkooporders vanuit Supply Chain Management met Sales mogelijk via de functie Gegevensintegratie.</span><span class="sxs-lookup"><span data-stu-id="92a37-125">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order synchronization from Supply Chain Management to Sales via the Data Integration feature.</span></span>

    > [!NOTE]
    > <span data-ttu-id="92a37-126">U hoeft alleen KB4045570 te installeren omdat de installatie de wijzigingen van andere hotfixes bevat.</span><span class="sxs-lookup"><span data-stu-id="92a37-126">You only have to install KB4045570 because the installation includes the changes from other hotfixes.</span></span> 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a><span data-ttu-id="92a37-127">Dynamics 365 for Finance and Operations versie 1611 (november 2016)</span><span class="sxs-lookup"><span data-stu-id="92a37-127">Dynamics 365 for Finance and Operations version 1611 (November 2016)</span></span>

- <span data-ttu-id="92a37-128">Dynamics 365 for Finance and Operations versie 1611 (november 2016) met Platform Update 8 of hoger</span><span class="sxs-lookup"><span data-stu-id="92a37-128">Dynamics 365 for Finance and Operations version 1611 (November 2016)  with platform update 8 or higher</span></span>

- <span data-ttu-id="92a37-129">De volgende hotfixes zijn vereist:</span><span class="sxs-lookup"><span data-stu-id="92a37-129">The following hotfixes are required:</span></span>

  - <span data-ttu-id="92a37-130">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)**: De synchronisatie van verkooporders met Gegevensintegrator van Supply Chain Management naar Sales inschakelen.</span><span class="sxs-lookup"><span data-stu-id="92a37-130">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Enable sales order synchronization with Data integrator from Supply Chain Management to Sales.</span></span> 
  - <span data-ttu-id="92a37-131">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)**: De synchronisatie van verkooporderkoppen en -regels met Gegevensintegrator van Supply Chain Management naar Sales inschakelen.</span><span class="sxs-lookup"><span data-stu-id="92a37-131">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Enable sales order header and line synchronization with Data integrator from Supply Chain Management to Sales.</span></span>
  - <span data-ttu-id="92a37-132">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)**: Ondersteuning voor de integratie van Prospect naar contant geld via gegevensentiteiten is vereist.</span><span class="sxs-lookup"><span data-stu-id="92a37-132">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Support for prospect to cash integration through data entities is required.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="92a37-133">Na installatie van de hotfixes moet u de volgende batchtaak triggeren vanuit het formulier **SalesPopulateProspectToCash**.</span><span class="sxs-lookup"><span data-stu-id="92a37-133">After you install the hotfixes, you must trigger the following batch job from the **SalesPopulateProspectToCash** form.</span></span> <span data-ttu-id="92a37-134">Dit formulier is verborgen omdat u het maar eenmaal nodig hebt.</span><span class="sxs-lookup"><span data-stu-id="92a37-134">This form is hidden because you only need it once.</span></span> <span data-ttu-id="92a37-135">U opent het formulier door u aan te melden bij de omgeving en het volgende aan de URL in uw browseradres toe te voegen: *&mi=action:SalesPopulateProspectToCash*, bijvoorbeeld `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span><span class="sxs-lookup"><span data-stu-id="92a37-135">To access the form, log in to the environment and add the following to the URL in your browser address: *&mi=action:SalesPopulateProspectToCash*, for example, `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span></span> <span data-ttu-id="92a37-136">Wanneer het formulier wordt geopend, klikt u op OK.</span><span class="sxs-lookup"><span data-stu-id="92a37-136">When the form opens, click OK.</span></span> <span data-ttu-id="92a37-137">In de tabellen **SalesLine**, **SalesQuotationLine** en **CustInvoiceTrans** wordt een nieuw veld **LineCreationSequnceNumber** gevuld met unieke waarden en de lijst met producten wordt vernieuwd.</span><span class="sxs-lookup"><span data-stu-id="92a37-137">This will populate a new **LineCreationSequnceNumber** field in the **SalesLine**, **SalesQuotationLine**, and **CustInvoiceTrans** tables with unique values, and the product list will be refreshed.</span></span> <span data-ttu-id="92a37-138">Dit is nodig voor een geslaagde integratie van Prospect naar contant geld.</span><span class="sxs-lookup"><span data-stu-id="92a37-138">This is required for the Prospect to cash integration to work.</span></span>


## <a name="system-requirements-for-sales"></a><span data-ttu-id="92a37-139">Systeemvereisten voor Sales</span><span class="sxs-lookup"><span data-stu-id="92a37-139">System requirements for Sales</span></span>

<span data-ttu-id="92a37-140">Als u de oplossing Prospect naar contant geld wilt gebruiken, moet u de volgende onderdelen installeren:</span><span class="sxs-lookup"><span data-stu-id="92a37-140">To use the Prospect to cash solution, you must install the following components:</span></span>

- <span data-ttu-id="92a37-141">Dynamics 365 Sales-versie 1612 (8.2.1.207) (DB 8.2.1.207) online of een hogere versie.</span><span class="sxs-lookup"><span data-stu-id="92a37-141">Dynamics 365 Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online or a later version</span></span>
- <span data-ttu-id="92a37-142">De oplossing Prospect naar contant geld voor Dynamics 365 Sales, versie 1.15.0.0 of een hogere versie.</span><span class="sxs-lookup"><span data-stu-id="92a37-142">Prospect to cash solution for Dynamics 365 Sales, version 1.15.0.0 or a later version.</span></span> <span data-ttu-id="92a37-143">De oplossing kan worden gedownload van AppSource.</span><span class="sxs-lookup"><span data-stu-id="92a37-143">The solution is available for download from AppSource.</span></span> <span data-ttu-id="92a37-144">[Download Dynamics 365, Prospect naar contant geld](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span><span class="sxs-lookup"><span data-stu-id="92a37-144">[Download Dynamics 365, Prospect to Cash](https://appsource.microsoft.com/product/dynamics-365/mscrm.c7a48b40-eed3-4d67-93ba-f2364281feb3).</span></span>
