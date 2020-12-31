---
title: SQL Server Reporting Services configureren voor on-premises implementaties
description: Dit onderwerp biedt informatie over het configureren van SQL Server Reporting Services (SSRS) voor een on-premises implementatie.
author: PeterRFriis
manager: AnnBe
ms.date: 06/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 55651
ms.assetid: ''
ms.search.region: Global
ms.author: perahlff
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.openlocfilehash: 2577705b04beef1f8b03f83ed8536be2e6ab6e83
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683916"
---
# <a name="configure-sql-server-reporting-services-for-on-premises-deployments"></a><span data-ttu-id="8c560-103">SQL Server Reporting Services configureren voor on-premises implementaties</span><span class="sxs-lookup"><span data-stu-id="8c560-103">Configure SQL Server Reporting Services for on-premises deployments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8c560-104">Volg de stappen in dit onderwerp om SQL Server Reporting Services (SSRS) te configureren voor uw (on-premises) implementatie van Microsoft Dynamics 365 Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="8c560-104">Use the steps in this topic to configure SQL Server Reporting Services (SSRS) for your Microsoft Dynamics 365 Finance + Operations (on-premises) deployment.</span></span>

1. <span data-ttu-id="8c560-105">Open de toepassing Reporting Services Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="8c560-105">Open the Reporting Services Configuration Manager application.</span></span>
2. <span data-ttu-id="8c560-106">Laat de standaard **servernaam**, gewoonlijk de naam van de huidige computer, en de **Naam van rapportserverexemplaar** **MSSQLSERVER** staan.</span><span class="sxs-lookup"><span data-stu-id="8c560-106">Leave the default **Server name**, which should be the name of the current machine, and the **Report Server Instance**, **MSSQLSERVER**.</span></span>
3. <span data-ttu-id="8c560-107">Klik op **Verbinden**.</span><span class="sxs-lookup"><span data-stu-id="8c560-107">Click **Connect**.</span></span>

    <span data-ttu-id="8c560-108">[![Configuratie verbinding Reporting Services](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span><span class="sxs-lookup"><span data-stu-id="8c560-108">[![Reporting services configuration connection](./media/ssrs-config-manager-01.png)](./media/ssrs-config-manager-01.png)</span></span>

4. <span data-ttu-id="8c560-109">Klik op het tabblad **Serviceaccount** en controleer of de instellingen overeenkomen met de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="8c560-109">Click the **Service Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="8c560-110">[![Tabbald Serviceaccount](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span><span class="sxs-lookup"><span data-stu-id="8c560-110">[![Service account tab](./media/ssrs-config-manager-02.png)](./media/ssrs-config-manager-02.png)</span></span>

5. <span data-ttu-id="8c560-111">Klik op het tabblad **Webservice-URL** en controleer of de instellingen overeenkomen met de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="8c560-111">Click the **Web Service URL** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="8c560-112">[![Tabblad Webservice-URL](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span><span class="sxs-lookup"><span data-stu-id="8c560-112">[![Web service URL tab](./media/ssrs-config-manager-03.png)](./media/ssrs-config-manager-03.png)</span></span>

6. <span data-ttu-id="8c560-113">Klik op het tabblad **Database** en controleer of **Databasenaam** en **Referentie-instellingen** overeenkomen met de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="8c560-113">Click the **Database** tab and verify that the **Database Name** and **Credential settings** match the following graphic.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8c560-114">U moet een nieuwe database maken.</span><span class="sxs-lookup"><span data-stu-id="8c560-114">You will need to create a new database.</span></span> <span data-ttu-id="8c560-115">Klik hiertoe op **Database wijzigen** en vervolgens controleert u of de naam van de nieuwe database als volgt luidt: **DynamicsAxReportServer**.</span><span class="sxs-lookup"><span data-stu-id="8c560-115">To do this, click **Change Database**, and then verify that the new database name is: **DynamicsAxReportServer**.</span></span>

    <span data-ttu-id="8c560-116">[![Tabblad Database](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span><span class="sxs-lookup"><span data-stu-id="8c560-116">[![database tab](./media/ssrs-config-manager-04.png)](./media/ssrs-config-manager-04.png)</span></span>

7. <span data-ttu-id="8c560-117">Klik op het tabblad **Webportal-URL** en controleer of de instellingen overeenkomen met de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="8c560-117">Click the **Web Portal URL** tab and verify that the settings match the following graphic.</span></span>

    > [!NOTE]
    > <span data-ttu-id="8c560-118">Klik op **Toepassen** om de Portal te maken en correct te configureren.</span><span class="sxs-lookup"><span data-stu-id="8c560-118">You must click **Apply** to create and properly configure the Portal.</span></span>

    <span data-ttu-id="8c560-119">[![Tabblad Webportal-url](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span><span class="sxs-lookup"><span data-stu-id="8c560-119">[![web portal url tab](./media/ssrs-config-manager-05.png)](./media/ssrs-config-manager-05.png)</span></span>

    <span data-ttu-id="8c560-120">Nadat de Portal is geconfigureerd, komt het tabblad **Webportal** overeen met de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="8c560-120">After the Portal is configured, the **Web Portal** tab will match the following graphic.</span></span>

    <span data-ttu-id="8c560-121">[![Tabblad Webportal](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span><span class="sxs-lookup"><span data-stu-id="8c560-121">[![web portal tab](./media/ssrs-config-manager-06.png)](./media/ssrs-config-manager-06.png)</span></span>

8. <span data-ttu-id="8c560-122">Klik op de URL van de rapporten om de webportal SQL Server Reporting Services weer te geven.</span><span class="sxs-lookup"><span data-stu-id="8c560-122">Click the reports URL to view the SQL Server Reporting Services web portal.</span></span>
9. <span data-ttu-id="8c560-123">Wanneer u zich in de portal bevindt, maakt u een nieuwe map met de naam **Dynamics**.</span><span class="sxs-lookup"><span data-stu-id="8c560-123">When you are in the portal, create a new folder named **Dynamics**.</span></span>

    <span data-ttu-id="8c560-124">[![Dynamics-map](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span><span class="sxs-lookup"><span data-stu-id="8c560-124">[![dynamics folder](./media/ssrs-config-manager-07.png)](./media/ssrs-config-manager-07.png)</span></span>

10. <span data-ttu-id="8c560-125">Klik in **Reporting Services Configuration Manager** op het tabblad **E-mailinstellingen** en controleer of de instellingen overeenkomen met de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="8c560-125">In the **Reporting Services Configuration Manager**, click the **E-mail Settings** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="8c560-126">[![Tabblad E-mailinstellingen](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span><span class="sxs-lookup"><span data-stu-id="8c560-126">[![email settings tab](./media/ssrs-config-manager-08.png)](./media/ssrs-config-manager-08.png)</span></span>

11. <span data-ttu-id="8c560-127">Klik op het tabblad **Uitvoeringsaccount** en controleer of de instellingen overeenkomen met de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="8c560-127">Click the **Execution Account** tab and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="8c560-128">[![Tabblad Uitvoeringsaccount](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span><span class="sxs-lookup"><span data-stu-id="8c560-128">[![execution account tab](./media/ssrs-config-manager-09.png)](./media/ssrs-config-manager-09.png)</span></span>

    <span data-ttu-id="8c560-129">Wijzig de standaardinstellingen op het tabblad **Coderingssleutels** niet.</span><span class="sxs-lookup"><span data-stu-id="8c560-129">Don't change the default settings on the **Encryption Keys** tab.</span></span>

    <span data-ttu-id="8c560-130">[![Tabblad Coderingssleutel](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span><span class="sxs-lookup"><span data-stu-id="8c560-130">[![encryption keys tab](./media/ssrs-config-manager-10.png)](./media/ssrs-config-manager-10.png)</span></span>

12. <span data-ttu-id="8c560-131">Klik op het tabblad **Abonnementen instellen** en controleer of de instellingen overeenkomen met de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="8c560-131">Click the **Subscription Settings** tab, and verify that the settings match the following graphic.</span></span>

    <span data-ttu-id="8c560-132">[![tabblad Abonnementen instellen](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span><span class="sxs-lookup"><span data-stu-id="8c560-132">[![subscription settings tab](./media/ssrs-config-manager-11.png)](./media/ssrs-config-manager-11.png)</span></span>

    <span data-ttu-id="8c560-133">Wijzig de standaardinstellingen op het tabblad **Implementatie horizontaal schalen** niet.</span><span class="sxs-lookup"><span data-stu-id="8c560-133">Don't change the default settings on the **Scale-out Deployment** tab.</span></span>

    <span data-ttu-id="8c560-134">[![Tabblad Implementatie horizontaal schalen](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span><span class="sxs-lookup"><span data-stu-id="8c560-134">[![scale-out deployment tab](./media/ssrs-config-manager-12.png)](./media/ssrs-config-manager-12.png)</span></span>

    <span data-ttu-id="8c560-135">Wijzig de standaardinstellingen op het tabblad **Power BI-integratie** niet.</span><span class="sxs-lookup"><span data-stu-id="8c560-135">Don't change the default settings on the **Power BI Integration** tab.</span></span>

    <span data-ttu-id="8c560-136">[![Tabblad Power BI-integratie](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span><span class="sxs-lookup"><span data-stu-id="8c560-136">[![power bi integration tab](./media/ssrs-config-manager-13.png)](./media/ssrs-config-manager-13.png)</span></span>

13. <span data-ttu-id="8c560-137">Klik op **Afsluiten** om de **Reporting Services Configuration Manager** te sluiten.</span><span class="sxs-lookup"><span data-stu-id="8c560-137">Click **Exit** to close the **Reporting Services Configuration Manager**.</span></span>

    <span data-ttu-id="8c560-138">[![Reporting Services Configuration Manager sluiten](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span><span class="sxs-lookup"><span data-stu-id="8c560-138">[![close reporting services configuration manager](./media/ssrs-config-manager-14.png)](./media/ssrs-config-manager-14.png)</span></span>
