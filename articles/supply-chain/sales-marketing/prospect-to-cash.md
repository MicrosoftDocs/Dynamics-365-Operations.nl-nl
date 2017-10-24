---
title: Prospect naar contant geld
description: Het onderwerp biedt een overzicht van de oplossing Prospect naar contant geld tussen Dynamics 365 for Finance and Operations, Enterprise edition en Dynamics 365 for Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: a5f1ecd5f8b46287839439a963e571531ae161a7
ms.contentlocale: nl-nl
ms.lasthandoff: 09/29/2017

---

# <a name="prospect-to-cash"></a><span data-ttu-id="ef460-103">Prospect naar contant geld</span><span class="sxs-lookup"><span data-stu-id="ef460-103">Prospect to cash</span></span>  

[!include[banner](../includes/banner.md)]

<span data-ttu-id="ef460-104">De oplossing Prospect naar contant geld gebruikt [Gegevensintegratie](/common-data-service/entity-reference/dynamics-365-integration) om gegevens te synchroniseren tussen exemplaren van Microsoft Dynamics 365 for Finance and Operations, Enterprise edition en Dynamics 365 for Sales via Common Data Service (CDS).</span><span class="sxs-lookup"><span data-stu-id="ef460-104">The Prospect to cash solution uses [Data Integration](/common-data-service/entity-reference/dynamics-365-integration) to synchronize data across Microsoft Dynamics 365 for Finance and Operations, Enterprise edition and Dynamics 365 for Sales instances via the Common Data Service (CDS).</span></span> <span data-ttu-id="ef460-105">De Prospect naar contant geld-sjablonen in de functie Gegevensintegratie activeren de stroom van gegevens over rekeningen, contactpersoon, producten, verkoopoffertes en verkoopfacturen tussen Finance and Operations en Sales.</span><span class="sxs-lookup"><span data-stu-id="ef460-105">The Prospect to cash templates available with the Data Integration feature enable the flow of accounts, contacts, products, sales quotes, sales orders, and sales invoices data between Finance and Operations and Sales.</span></span> <span data-ttu-id="ef460-106">Terwijl de gegevens tussen Finance and Operations en Sales worden verplaatst, kunt u verkoop- en marketingactiviteiten uitvoeren in Sales en de orderafhandeling verwerken met voorraadbeheer in Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ef460-106">While the data is flowing between Finance and Operations and Sales, you can carry out sales and marketing activities in Sales and handle the order fulfillment with inventory management in Finance and Operations.</span></span> 

<span data-ttu-id="ef460-107">Deze oplossing biedt integratie in de volgende gebieden:</span><span class="sxs-lookup"><span data-stu-id="ef460-107">This solution provides integration in the following areas:</span></span> 

-   [<span data-ttu-id="ef460-108">Rekeningen in Sales onderhouden en ze synchroniseren met Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ef460-108">Maintain accounts in Sales and sync them to Finance and Operations</span></span>](accounts-template-mapping.md)
-   [<span data-ttu-id="ef460-109">Contactpersonen in Sales onderhouden en ze synchroniseren met Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ef460-109">Maintain contacts in Sales and sync them to Finance and Operations</span></span>](contacts-template-mapping.md)
-   [<span data-ttu-id="ef460-110">Producten in Finance and Operations onderhouden en ze synchroniseren met Sales</span><span class="sxs-lookup"><span data-stu-id="ef460-110">Maintain products in Finance and Operations and sync them to Sales</span></span>](products-template-mapping.md)
-   [<span data-ttu-id="ef460-111">Verkoopoffertes maken in Sales en ze synchroniseren met Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="ef460-111">Create sales quotes in Sales and sync them to Finance and Operations</span></span>](sales-quotation-template-mapping.md)
-   [<span data-ttu-id="ef460-112">Verkooporders maken in Finance and Operations en ze synchroniseren met Sales</span><span class="sxs-lookup"><span data-stu-id="ef460-112">Create sales orders in Finance and Operations and sync them to Sales</span></span>](sales-order-template-mapping.md)
-   [<span data-ttu-id="ef460-113">Verkoopfacturen maken in Finance and Operations en ze synchroniseren met Sales</span><span class="sxs-lookup"><span data-stu-id="ef460-113">Create sales invoices in Finance and Operations and sync them to Sales</span></span>](sales-invoice-template-mapping.md)

## <a name="system-requirements-for-dynamics-365-for-finance-and-operations-enterprise-edition"></a><span data-ttu-id="ef460-114">Systeemvereisten voor Dynamics 365 for Finance and Operations, Enterprise edition</span><span class="sxs-lookup"><span data-stu-id="ef460-114">System requirements for Dynamics 365 for Finance and Operations, Enterprise edition</span></span>

<span data-ttu-id="ef460-115">Als u de oplossing Prospect naar contant geld wilt gebruiken, moet u het volgende installeren:</span><span class="sxs-lookup"><span data-stu-id="ef460-115">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="ef460-116">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (juli 2017) met platformupdate 8 (App 7.2.11792.56024 met platform 7.0.4565.16212)</span><span class="sxs-lookup"><span data-stu-id="ef460-116">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) with Platform update 8 (App 7.2.11792.56024 w/ Platform 7.0.4565.16212)</span></span>

- <span data-ttu-id="ef460-117">Twee hotfixes voor Dynamics 365 for Finance and Operations, Enterprise edition (juli 2017).</span><span class="sxs-lookup"><span data-stu-id="ef460-117">Two hotfixes for Dynamics 365 for Finance and Operations, Enterprise edition (July 2017).</span></span>

    -  <span data-ttu-id="ef460-118">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2): met deze hotfix kunnen verkooporderregels met de functie Gegevensintegratie van Finance and Operations met Sales worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="ef460-118">[KB4036524](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036524&bugId=3847504&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order line synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
        
    -  <span data-ttu-id="ef460-119">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2): met deze hotfix kunnen verkooporders met de functie Gegevensintegratie van Finance and Operations met Sales worden gesynchroniseerd.</span><span class="sxs-lookup"><span data-stu-id="ef460-119">[KB4036461](https://fix.lcs.dynamics.com/Issue/Resolved?kb=4036461&bugId=3847029&qc=e2fcfae08b1a5d5ce9f53f330e8c212b0636c375368ff7d8d9b5ec6701523ad2) - This hotfix enables sales order synchronization with the Data Integration feature from Finance and Operations to Sales.</span></span>
    
<span data-ttu-id="ef460-120">**Opmerking**: u hoeft alleen KB4036524 te installeren omdat de installatie de wijzigingen van KB4036461 bevat.</span><span class="sxs-lookup"><span data-stu-id="ef460-120">**Note**: You only need to install KB4036524 because the installation includes the changes from KB4036461.</span></span>
 
## <a name="system-requirements-for-dynamics-365-for-sales"></a><span data-ttu-id="ef460-121">Systeemvereisten voor Dynamics 365 for Sales</span><span class="sxs-lookup"><span data-stu-id="ef460-121">System requirements for Dynamics 365 for Sales</span></span>

<span data-ttu-id="ef460-122">Als u de oplossing Prospect naar contant geld wilt gebruiken, moet u het volgende installeren:</span><span class="sxs-lookup"><span data-stu-id="ef460-122">To use the Prospect to cash solution, you must install the following:</span></span>

- <span data-ttu-id="ef460-123">Dynamics 365 for Sales-versie 1612 (8.2.1.207) (DB 8.2.1.207) online of hoger.</span><span class="sxs-lookup"><span data-stu-id="ef460-123">Dynamics 365 for Sales version 1612 (8.2.1.207) (DB 8.2.1.207) online or later.</span></span>
- <span data-ttu-id="ef460-124">De oplossing Prospect naar contant geld voor Dynamics 365 for Sales, versie 1.14.0.0 (v14) of hoger.</span><span class="sxs-lookup"><span data-stu-id="ef460-124">Prospect to cash solution for Dynamics 365 for Sales, version 1.14.0.0 (v14) or later.</span></span>

### <a name="install-the-prospect-to-cash-solution-for-sales"></a><span data-ttu-id="ef460-125">De oplossing Prospect naar contant geld voor Sales installeren</span><span class="sxs-lookup"><span data-stu-id="ef460-125">Install the Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="ef460-126">Download het [zipbestand met de oplossing Prospect naar contant geld voor Dynamics 365 for Sales](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) op CustomerSource.</span><span class="sxs-lookup"><span data-stu-id="ef460-126">Download the [Prospect to cash for Dynamics 365 for Sales solution package zip file](https://mbs.microsoft.com/customersource/Global/365Enterprise/downloads/product-releases/MD365FNOPENTProspectToCash) on CustomerSource.</span></span>

- <span data-ttu-id="ef460-127">Zorg ervoor dat het zipbestand niet wordt geblokkeerd om te voorkomen dat het foutbericht Er zijn geen importpakketten gevonden wordt weergegeven wanneer u het oplossingspakket installeert.</span><span class="sxs-lookup"><span data-stu-id="ef460-127">Make sure that the zip file is unblocked so that you do not get the error message "No import packages were found" when you install the solution package.</span></span> <span data-ttu-id="ef460-128">Ga als volgt te werk om de blokkering van het bestand op te heffen:</span><span class="sxs-lookup"><span data-stu-id="ef460-128">To unblock the file, do the following:</span></span>

    -  <span data-ttu-id="ef460-129">Klik met de rechtermuisknop op het zipbestand.</span><span class="sxs-lookup"><span data-stu-id="ef460-129">Right-click the zip file.</span></span>
    -  <span data-ttu-id="ef460-130">Selecteer **Eigenschappen** en selecteer vervolgens **Deblokkeren**.</span><span class="sxs-lookup"><span data-stu-id="ef460-130">Select **Properties** and then select **Unblock**.</span></span> 

- <span data-ttu-id="ef460-131">Pak het zipbestand uit en voer PackageDeployer.exe uit.</span><span class="sxs-lookup"><span data-stu-id="ef460-131">Unzip and run PackageDeployer.exe.</span></span>

- <span data-ttu-id="ef460-132">Installeer de oplossing Prospect naar contant geld in uw exemplaar van Sales.</span><span class="sxs-lookup"><span data-stu-id="ef460-132">Install the Prospect to Cash solution in your Sales instance.</span></span>

    - <span data-ttu-id="ef460-133">Selecteer het implementatietype **Office 365**.</span><span class="sxs-lookup"><span data-stu-id="ef460-133">Select the **Office 365** Deployment type.</span></span>
    - <span data-ttu-id="ef460-134">Selecteer **Geavanceerd weergeven**.</span><span class="sxs-lookup"><span data-stu-id="ef460-134">Select **Show advanced**.</span></span>
    - <span data-ttu-id="ef460-135">Selecteer een **regio** voor een snelle installatie.</span><span class="sxs-lookup"><span data-stu-id="ef460-135">For a quick installation, select a **Region**.</span></span> <span data-ttu-id="ef460-136">Als u **Geen idee** selecteert, worden alle regio's gezocht en duurt de installatie langer.</span><span class="sxs-lookup"><span data-stu-id="ef460-136">If you select **Don’t know**, the system searches for all regions and it will take longer to install.</span></span>
    - <span data-ttu-id="ef460-137">Voer de **gebruikersnaam** en het **wachtwoord** voor een beheerder in die over de gebruikersrechten beschikt om te installeren.</span><span class="sxs-lookup"><span data-stu-id="ef460-137">Enter **User name** and **Password** for an admin user who has the user rights to install.</span></span>

