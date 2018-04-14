---
title: SQL Server Reporting Services configureren voor een on-premises implementatie
description: Dit onderwerp biedt informatie over het configureren van SQL Server Reporting Services (SSRS) voor een on-premises implementatie.
author: sarvanisathish
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Operations
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: sarvanis
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: bea198488da52de21aba0c33b4004b6ad7518fd3
ms.contentlocale: nl-nl
ms.lasthandoff: 04/13/2018

---
# <a name="configure-sql-server-reporting-services-for-an-on-premises-deployment"></a><span data-ttu-id="6e12a-103">SQL Server Reporting Services configureren voor een on-premises implementatie</span><span class="sxs-lookup"><span data-stu-id="6e12a-103">Configure SQL Server Reporting Services for an on-premises deployment</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="6e12a-104">Gebruik de stappen in dit onderwerp voor het configureren van SQL Server Reporting Services (SSRS) voor uw implementatie van Microsoft Dynamics 365 for Finance and Operations (on-premises).</span><span class="sxs-lookup"><span data-stu-id="6e12a-104">Use the steps in this topic to configure SQL Server Reporting Services (SSRS) for your Microsoft Dynamics 365 for Finance and Operations (on-premises) deployment.</span></span>

1. <span data-ttu-id="6e12a-105">Open de toepassing Reporting Services Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="6e12a-105">Open the Reporting Services Configuration Manager application.</span></span>
2. <span data-ttu-id="6e12a-106">Laat de standaard **servernaam**, gewoonlijk de naam van de huidige computer, en de **Naam van rapportserverexemplaar** **MSSQLSERVER** staan.</span><span class="sxs-lookup"><span data-stu-id="6e12a-106">Leave the default **Server name**, which should be the name of the current machine, and the **Report Server Instance**, **MSSQLSERVER**.</span></span> 
3. <span data-ttu-id="6e12a-107">Klik op **Verbinden**.</span><span class="sxs-lookup"><span data-stu-id="6e12a-107">Click **Connect**.</span></span>
   
   <span data-ttu-id="6e12a-108">[![Configuratie verbinding Reporting Services](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span><span class="sxs-lookup"><span data-stu-id="6e12a-108">[![Reporting services configuration connection](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span></span>
   
4. <span data-ttu-id="6e12a-109">Klik op het tabblad **Serviceaccount** en controleer of de instellingen overeenkomen met de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="6e12a-109">Click the **Service Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="6e12a-110">[![Tabbald Serviceaccount](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span><span class="sxs-lookup"><span data-stu-id="6e12a-110">[![Service account tab](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span></span>
    
5. <span data-ttu-id="6e12a-111">Klik op het tabblad **Webservice-URL** en controleer of de instellingen overeenkomen met de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="6e12a-111">Click the **Web Service URL** tab and verify that the settings match the following graphic.</span></span> 

    <span data-ttu-id="6e12a-112">[![Tabblad Webservice-URL](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span><span class="sxs-lookup"><span data-stu-id="6e12a-112">[![Web service URL tab](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span></span> 
    
6. <span data-ttu-id="6e12a-113">Klik op het tabblad **Database** en controleer of **Databasenaam** en **Referentie-instellingen** overeenkomen met de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="6e12a-113">Click the **Database** tab and verify that the **Database Name** and **Credential settings** match the following graphic.</span></span> <span data-ttu-id="6e12a-114">**Opmerking:** U moet een nieuwe database maken.</span><span class="sxs-lookup"><span data-stu-id="6e12a-114">**Note:** You will need to create a new database.</span></span> <span data-ttu-id="6e12a-115">Klik hiertoe op **Database wijzigen** en vervolgens controleert u of de naam van de nieuwe database als volgt luidt: **DynamicsAxReportServer**.</span><span class="sxs-lookup"><span data-stu-id="6e12a-115">To do this, click **Change Database**, and then verify that the new database name is: **DynamicsAxReportServer**.</span></span>

    <span data-ttu-id="6e12a-116">[![Tabblad Database](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span><span class="sxs-lookup"><span data-stu-id="6e12a-116">[![database tab](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span></span>
    
7. <span data-ttu-id="6e12a-117">Klik op het tabblad **Webportal-URL** en controleer of de instellingen overeenkomen met de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="6e12a-117">Click the **Web Portal URL** tab and verify that the settings match the following graphic.</span></span> <span data-ttu-id="6e12a-118">**Opmerking:** Klik op **Toepassen** om de Portal te maken en correct te configureren.</span><span class="sxs-lookup"><span data-stu-id="6e12a-118">**Note:** You must click **Apply** to create and properly configure the Portal.</span></span>

    <span data-ttu-id="6e12a-119">[![Tabblad Webportal-url](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span><span class="sxs-lookup"><span data-stu-id="6e12a-119">[![web portal url tab](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span></span>
    
   <span data-ttu-id="6e12a-120">Nadat de Portal is geconfigureerd, komt het tabblad **Webportal** overeen met de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="6e12a-120">After the Portal is configured, the **Web Portal** tab will match the following graphic.</span></span>
    <span data-ttu-id="6e12a-121">[![Tabblad Webportal](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span><span class="sxs-lookup"><span data-stu-id="6e12a-121">[![web portal tab](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span></span>
    
8. <span data-ttu-id="6e12a-122">Klik op de URL van de rapporten om de webportal SQL Server Reporting Services weer te geven.</span><span class="sxs-lookup"><span data-stu-id="6e12a-122">Click the reports URL to view the SQL Server Reporting Services web portal.</span></span> 
9. <span data-ttu-id="6e12a-123">Wanneer u zich in de portal bevindt, maakt u een nieuwe map met de naam **Dynamics**.</span><span class="sxs-lookup"><span data-stu-id="6e12a-123">When you are in the portal, create a new folder named **Dynamics**.</span></span>

   <span data-ttu-id="6e12a-124">[![Dynamics-map](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span><span class="sxs-lookup"><span data-stu-id="6e12a-124">[![dynamics folder](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span></span>
    
10. <span data-ttu-id="6e12a-125">Klik in **Reporting Services Configuration Manager** op het tabblad **E-mailinstellingen** en controleer of de instellingen overeenkomen met de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="6e12a-125">In the **Reporting Services Configuration Manager**, click the **E-mail Settings** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="6e12a-126">[![Tabblad E-mailinstellingen](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span><span class="sxs-lookup"><span data-stu-id="6e12a-126">[![email settings tab](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span></span>
    
11. <span data-ttu-id="6e12a-127">Klik op het tabblad **Uitvoeringsaccount** en controleer of de instellingen overeenkomen met de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="6e12a-127">Click the **Execution Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="6e12a-128">[![Tabblad Uitvoeringsaccount](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span><span class="sxs-lookup"><span data-stu-id="6e12a-128">[![execution account tab](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span></span>
    
    <span data-ttu-id="6e12a-129">Wijzig niet de standaardinstellingen op het tabblad **Coderingssleutel**. [![Tabblad Coderingssleutel](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span><span class="sxs-lookup"><span data-stu-id="6e12a-129">Don’t change the default settings on the **Encryption Keys** tab. [![encryption keys tab](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span></span>
    
12. <span data-ttu-id="6e12a-130">Klik op het tabblad **Abonnementen instellen** en controleer of de instellingen overeenkomen met de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="6e12a-130">Click the **Subscription Settings** tab, and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="6e12a-131">[![tabblad Abonnementen instellen](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span><span class="sxs-lookup"><span data-stu-id="6e12a-131">[![subscription settings tab](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span></span>
    
    <span data-ttu-id="6e12a-132">Wijzig niet de standaardinstellingen op het tabblad **Implementatie horizontaal schalen**. [![Tabblad Implementatie horizontaal schalen](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span><span class="sxs-lookup"><span data-stu-id="6e12a-132">Don’t change the default settings on the **Scale-out Deployment** tab. [![scale-out deployment tab](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span></span>
    
    <span data-ttu-id="6e12a-133">Wijzig niet de standaardinstellingen op het tabblad **Power BI-integratie**. [![Tabblad Power BI-integratie](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span><span class="sxs-lookup"><span data-stu-id="6e12a-133">Don’t change the default settings on the **Power BI Integration** tab. [![power bi integration tab](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span></span> 
    
13. <span data-ttu-id="6e12a-134">Klik op **Afsluiten** om de **Reporting Services Configuration Manager** te sluiten.</span><span class="sxs-lookup"><span data-stu-id="6e12a-134">Click **Exit** to close the **Reporting Services Configuration Manager**.</span></span>

    <span data-ttu-id="6e12a-135">[![Reporting Services Configuration Manager sluiten](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span><span class="sxs-lookup"><span data-stu-id="6e12a-135">[![close reporting services configuration manager](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span></span>
    


