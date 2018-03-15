---
title: Prospect naar contant geld
description: Dit onderwerp biedt een overzicht van de oplossing Prospect naar contant geld tussen Microsoft Dynamics 365 for Finance and Operations, Enterprise edition en Microsoft Dynamics 365 for Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 02/08/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, SalesTable, EcoResProductListPage
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 95d5bf26c22238753586cf4a7aaf5c26f061a705
ms.openlocfilehash: 62f328c5a6bf5343c97de0b7d907bbcfe2fcde4d
ms.contentlocale: nl-nl
ms.lasthandoff: 02/23/2018

---

# <a name="prospect-to-cash"></a><span data-ttu-id="a45d4-103">Prospect naar contant geld</span><span class="sxs-lookup"><span data-stu-id="a45d4-103">Prospect to cash</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="a45d4-104">De oplossing Prospect naar contant geld biedt directe synchronisatie tussen Dynamics 365 for Finance and Operations, Enterprise-editie en Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="a45d4-104">The Prospect to cash solution provides direct synchronization across Dynamics 365 for Finance and Operations, Enterprise edition, and Dynamics 365 for Sales.</span></span> <span data-ttu-id="a45d4-105">De Prospect naar contant geld-sjablonen die beschikbaar zijn in de functie Gegevensintegratie activeren de stroom van gegevens voor rekeningen, contactpersonen, producten, verkoopoffertes en verkoopfacturen tussen Finance and Operations en Sales.</span><span class="sxs-lookup"><span data-stu-id="a45d4-105">The Prospect to cash templates that are available with the Data Integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="a45d4-106">Terwijl de gegevens tussen Finance and Operations en Sales worden verplaatst, kunt u verkoop- en marketingactiviteiten uitvoeren in Sales en de orderafhandeling verwerken met voorraadbeheer in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a45d4-106">While data is flowing between Finance and Operations and Sales, you can perform sales and marketing activities in Sales, and you can handle order fulfillment by using inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="a45d4-107">Bekijk de korte YouTube-video voor meer informatie over de integratie van Prospect met contant geld:</span><span class="sxs-lookup"><span data-stu-id="a45d4-107">For more information about the Prospect to cash integration, watch the short YouTube video:</span></span>

> [!Video https://www.youtube.com/embed/AVV9x5x-XCg]

<span data-ttu-id="a45d4-108">In de huidige versie biedt de oplossing Prospect naar contant geld de volgende typen directe synchronisatie:</span><span class="sxs-lookup"><span data-stu-id="a45d4-108">In the current version, the Prospect to cash solution provides the following types of direct synchronization:</span></span>

- [<span data-ttu-id="a45d4-109">Rekeningen in Sales onderhouden en direct vanuit Sales naar Finance and Operations synchroniseren</span><span class="sxs-lookup"><span data-stu-id="a45d4-109">Maintain accounts in Sales and sync them directly from Sales to Finance and Operations</span></span>](accounts-template-mapping-direct.md)
- [<span data-ttu-id="a45d4-110">Producten in Finance and Operations onderhouden en direct synchroniseren met Sales</span><span class="sxs-lookup"><span data-stu-id="a45d4-110">Maintain products in Finance and Operations and sync them directly to Sales</span></span>](products-template-mapping-direct.md)
- [<span data-ttu-id="a45d4-111">Contactpersonen in Sales onderhouden en direct synchroniseren met contactpersonen of klanten in Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a45d4-111">Maintain contacts in Sales and sync them directly to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)
- [<span data-ttu-id="a45d4-112">Verkoopoffertes vanuit Sales direct synchroniseren naar Finance and Operations (sjabloon in afwachting van vrijgave)</span><span class="sxs-lookup"><span data-stu-id="a45d4-112">Synchronize sales quotation directly from Sales to Finance and Operations (template pending release)</span></span>](sales-quotation-template-mapping-sales-fin.md)
- [<span data-ttu-id="a45d4-113">Verkooporders vanuit Finance and Operations rechtstreeks synchroniseren met Sales</span><span class="sxs-lookup"><span data-stu-id="a45d4-113">Synchronize sales orders directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct.md)
- [<span data-ttu-id="a45d4-114">Verkooporders rechtstreeks synchroniseren tussen Sales en Finance and Operations (sjabloon in afwachting van vrijgave)</span><span class="sxs-lookup"><span data-stu-id="a45d4-114">Synchronize sales orders directly between Sales and Finance and Operations (template pending release)</span></span>](sales-order-template-mapping-direct-two-ways.md)
- [<span data-ttu-id="a45d4-115">Verkoopfacturen vanuit Finance and Operations rechtstreeks synchroniseren met Sales</span><span class="sxs-lookup"><span data-stu-id="a45d4-115">Synchronize sales invoice directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)

## <a name="system-requirements-for-finance-and-operations"></a><span data-ttu-id="a45d4-116">Systeemvereisten voor Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a45d4-116">System requirements for Finance and Operations</span></span>

<span data-ttu-id="a45d4-117">Integratie van Prospect met contant geld wordt ondersteund door de volgende versies:</span><span class="sxs-lookup"><span data-stu-id="a45d4-117">Prospect to cash integration is supported on the following versions:</span></span>

### <a name="microsoft-dynamics-365-for-finance-and-operations-enterprise-edition-73-december-2017"></a><span data-ttu-id="a45d4-118">Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 (december 2017)</span><span class="sxs-lookup"><span data-stu-id="a45d4-118">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 (December 2017)</span></span>

- <span data-ttu-id="a45d4-119">Dynamics 365 for Finance and Operations, Enterprise Edition (december 2017) - toepassingsbuild 7.3.11971.56116 met platformupdate 12 (7.0.4709.41129)</span><span class="sxs-lookup"><span data-stu-id="a45d4-119">Dynamics 365 for Finance and Operations, Enterprise edition (December 2017) - Application build 7.3.11971.56116 with Platform Update 12 (7.0.4709.41129)</span></span>

### <a name="dynamics-365-for-finance-and-operations-enterprise-edition-july-2017"></a><span data-ttu-id="a45d4-120">Dynamics 365 for Finance and Operations, Enterprise-editie (juli 2017)</span><span class="sxs-lookup"><span data-stu-id="a45d4-120">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017)</span></span>

- <span data-ttu-id="a45d4-121">Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017) - met platformupdate 8 (toepassingsbuild 7.2.11792.56024 met platformbuild 7.0.4565.16212).</span><span class="sxs-lookup"><span data-stu-id="a45d4-121">Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) - with platform update 8 (application build 7.2.11792.56024 with platform build 7.0.4565.16212).</span></span>
- <span data-ttu-id="a45d4-122">De volgende hotfixes zijn vereist:</span><span class="sxs-lookup"><span data-stu-id="a45d4-122">The following hotfixes are required:</span></span>

    - <span data-ttu-id="a45d4-123">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)**: met deze hotfix kunnen verkooporders met de functie Gegevensintegratie van Sales naar Finance and Operations worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="a45d4-123">**[KB4045570](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4045570&bugId=3851320&qc=ac1145034fd04ab71ccc4d14aa012f245176712c9af7c36bb77a118726d46160)** – This hotfix enables sales order synchronization from Sales to Finance and Operations via the Data Integration feature.</span></span> <span data-ttu-id="a45d4-124">Daarnaast bevat de hotfix diverse andere verbeteringen.</span><span class="sxs-lookup"><span data-stu-id="a45d4-124">It also provides several other enhancements.</span></span>
    - <span data-ttu-id="a45d4-125">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)**: met deze hotfix kunnen verkooporderregels met de functie Gegevensintegratie van Finance and Operations naar Sales worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="a45d4-125">**[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order line synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>
    - <span data-ttu-id="a45d4-126">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)**: met deze hotfix kunnen verkooporders met de functie Gegevensintegratie van Finance and Operations naar Sales worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="a45d4-126">**[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2)** – This hotfix enables sales order synchronization from Finance and Operations to Sales via the Data Integration feature.</span></span>

    > [!NOTE]
    > <span data-ttu-id="a45d4-127">U hoeft alleen KB4045570 te installeren omdat de installatie de wijzigingen van andere hotfixes bevat.</span><span class="sxs-lookup"><span data-stu-id="a45d4-127">You only have to install KB4045570 because the installation includes the changes from other hotfixes.</span></span> 

### <a name="dynamics-365-for-finance-and-operations-version-1611-november-2016"></a><span data-ttu-id="a45d4-128">Versie 1611 van Dynamics 365 for Finance and Operations (november 2016)</span><span class="sxs-lookup"><span data-stu-id="a45d4-128">Dynamics 365 for Finance and Operations version 1611 (November 2016)</span></span>

- <span data-ttu-id="a45d4-129">Versie 1611 van Dynamics 365 for Finance and Operations (november 2016) met platformupdate 8 of hoger</span><span class="sxs-lookup"><span data-stu-id="a45d4-129">Dynamics 365 for Finance and Operations version 1611 (November 2016)  with platform update 8 or higher</span></span>

- <span data-ttu-id="a45d4-130">De volgende hotfixes zijn vereist:</span><span class="sxs-lookup"><span data-stu-id="a45d4-130">The following hotfixes are required:</span></span>

    - <span data-ttu-id="a45d4-131">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)**: De synchronisatie van verkooporders met Gegevensintegrator van Finance and Operations naar Sales inschakelen.</span><span class="sxs-lookup"><span data-stu-id="a45d4-131">**[KB4051266](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4051266&bugId=3863566&qc=ee80faaa7bc6c77b368d5eaf456c9c08e0b9fba5903a7b6fd8c13756c3a4b757)** - Enable sales order synchronization with Data integrator from Finance and Operations to Sales.</span></span> 
    - <span data-ttu-id="a45d4-132">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)**: De synchronisatie van kopteksten en regels van verkooporders met Gegevensintegrator van Finance and Operations naar Sales inschakelen.</span><span class="sxs-lookup"><span data-stu-id="a45d4-132">**[KB4037542](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4037542&bugId=3848253&qc=8323b93c15280172c5ab4159e0256e37104ced1729462c91ab2f7d00cb8d419c)** - Enable sales order header and line synchronization with Data integrator from Finance and Operations to Sales.</span></span>
    - <span data-ttu-id="a45d4-133">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)**: Ondersteuning voor de integratie van Prospect naar contant geld via gegevensentiteiten is vereist.</span><span class="sxs-lookup"><span data-stu-id="a45d4-133">**[KB4033093](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4033093&bugId=3824604&qc=bd7e15e1fb56066b3a82ce48b691cf1ffbc934a7473fa888545b2211a8d416c5)** - Support for prospect to cash integration through data entities is required.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="a45d4-134">Na installatie van de hotfixes moet u de volgende batchtaak triggeren vanuit het formulier **SalesPopulateProspectToCash**.</span><span class="sxs-lookup"><span data-stu-id="a45d4-134">After you install the hotfixes, you must trigger the following batch job from the **SalesPopulateProspectToCash** form.</span></span> <span data-ttu-id="a45d4-135">Dit formulier is verborgen omdat u het maar eenmaal nodig hebt.</span><span class="sxs-lookup"><span data-stu-id="a45d4-135">This form is hidden because you only need it once.</span></span> <span data-ttu-id="a45d4-136">U opent het formulier door u aan te melden bij de omgeving en het volgende aan de URL in uw browseradres toe te voegen: &mi=action:SalesPopulateProspectToCash, bijvoorbeeld `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span><span class="sxs-lookup"><span data-stu-id="a45d4-136">To access the form, log in to the environment and add the following to the URL in your browser address: &mi=action:SalesPopulateProspectToCash, for example, `https://ax123456.cloud.test.dynamics.com/?cmp=USMF&mi=action:SalesPopulateProspectToCash`.</span></span> <span data-ttu-id="a45d4-137">Wanneer het formulier wordt geopend, klikt u op OK.</span><span class="sxs-lookup"><span data-stu-id="a45d4-137">When the form opens, click OK.</span></span> <span data-ttu-id="a45d4-138">In de tabellen **SalesLine**, **SalesQuotationLine** en **CustInvoiceTrans** wordt een nieuw veld **LineCreationSequnceNumber** gevuld met unieke waarden en de lijst met producten wordt vernieuwd.</span><span class="sxs-lookup"><span data-stu-id="a45d4-138">This will populate a new **LineCreationSequnceNumber** field in the **SalesLine**, **SalesQuotationLine**, and **CustInvoiceTrans** tables with unique values, and the product list will be refreshed.</span></span> <span data-ttu-id="a45d4-139">Dit is nodig voor een geslaagde integratie van Prospect naar contant geld.</span><span class="sxs-lookup"><span data-stu-id="a45d4-139">This is required for the Prospect to cash integration to work.</span></span>


## <a name="system-requirements-for-sales"></a><span data-ttu-id="a45d4-140">Systeemvereisten voor Sales</span><span class="sxs-lookup"><span data-stu-id="a45d4-140">System requirements for Sales</span></span>

<span data-ttu-id="a45d4-141">Als u de oplossing Prospect naar contant geld wilt gebruiken, moet u de volgende onderdelen installeren:</span><span class="sxs-lookup"><span data-stu-id="a45d4-141">To use the Prospect to cash solution, you must install the following components:</span></span>

- <span data-ttu-id="a45d4-142">Dynamics 365 for Sales-versie 1612 (8.2.1.207) (DB 8.2.1.207) online</span><span class="sxs-lookup"><span data-stu-id="a45d4-142">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online</span></span>
- <span data-ttu-id="a45d4-143">De oplossing Prospect naar contant geld voor Dynamics 365 for Sales, versie 1.15.0.0 (v15)</span><span class="sxs-lookup"><span data-stu-id="a45d4-143">Prospect to cash solution for Dynamics 365 for Sales, version 1.15.0.0 (v15)</span></span> 

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="a45d4-144">De oplossing Prospect naar contant geld voor Sales installeren</span><span class="sxs-lookup"><span data-stu-id="a45d4-144">Install the Prospect to cash solution for Sales</span></span>

1. <span data-ttu-id="a45d4-145">Download het [zipbestand met de oplossing Prospect naar contant geld voor Dynamics 365 for Sales](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) van CustomerSource.</span><span class="sxs-lookup"><span data-stu-id="a45d4-145">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) from CustomerSource.</span></span>
2. <span data-ttu-id="a45d4-146">Zorg ervoor dat het zipbestand niet wordt geblokkeerd.</span><span class="sxs-lookup"><span data-stu-id="a45d4-146">Make sure that the zip file is unblocked.</span></span> <span data-ttu-id="a45d4-147">Anders wordt mogelijk het foutbericht Er zijn geen importpakketten gevonden weergegeven wanneer u het oplossingspakket installeert.</span><span class="sxs-lookup"><span data-stu-id="a45d4-147">Otherwise, when you try to install the solution package, you may receive the following error message, "No import packages were found."</span></span> <span data-ttu-id="a45d4-148">Als u het zipbestand wilt deblokkeren, klikt u er met de rechtermuisknop op en selecteert u **Eigenschappen**.</span><span class="sxs-lookup"><span data-stu-id="a45d4-148">To unblock the zip file, right-click it, and select **Properties**.</span></span> <span data-ttu-id="a45d4-149">Selecteer **Deblokkeren**.</span><span class="sxs-lookup"><span data-stu-id="a45d4-149">Select **Unblock**.</span></span>
3. <span data-ttu-id="a45d4-150">Pak het zipbestand uit en voer **PackageDeployer.exe** uit.</span><span class="sxs-lookup"><span data-stu-id="a45d4-150">Unzip and run **PackageDeployer.exe**.</span></span>
4. <span data-ttu-id="a45d4-151">Installeer de oplossing Prospect naar contant geld in uw exemplaar van Sales:</span><span class="sxs-lookup"><span data-stu-id="a45d4-151">Install the Prospect to cash solution on your Sales instance:</span></span>

    1. <span data-ttu-id="a45d4-152">Selecteer **Office 365** als het implementatietype.</span><span class="sxs-lookup"><span data-stu-id="a45d4-152">Select **Office 365** as the deployment type.</span></span>
    2. <span data-ttu-id="a45d4-153">Selecteer **Geavanceerd weergeven**.</span><span class="sxs-lookup"><span data-stu-id="a45d4-153">Select **Show advanced**.</span></span>
    3. <span data-ttu-id="a45d4-154">Selecteer een regio voor een snelle installatie.</span><span class="sxs-lookup"><span data-stu-id="a45d4-154">For a quick installation, select a region.</span></span> <span data-ttu-id="a45d4-155">Als u **Geen idee** selecteert, worden alle regio's gezocht en duurt de installatie langer.</span><span class="sxs-lookup"><span data-stu-id="a45d4-155">If you select **Don't know**, the system searches for all regions, and the installation will take more time.</span></span>
    4. <span data-ttu-id="a45d4-156">Voer de gebruikersnaam en het wachtwoord in voor een beheerder die over installatierechten beschikt.</span><span class="sxs-lookup"><span data-stu-id="a45d4-156">Enter the user name and password of an admin user who has installation rights.</span></span>



