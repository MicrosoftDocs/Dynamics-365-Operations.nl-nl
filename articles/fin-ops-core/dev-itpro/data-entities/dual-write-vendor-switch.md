---
title: Schakelen tussen leverancierontwerpen
description: In dit onderwerp wordt beschreven hoe u schakelt tussen de integratie van leveranciersgegevens tussen Finance and Operations-apps en Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 204d788e72e79e7acf744d24cbeacb0f9b47da7d
ms.sourcegitcommit: 3306e451f04df01c51d8d332306b135d8ae1e254
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 12/09/2019
ms.locfileid: "2902720"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="cfb7f-103">Schakelen tussen leverancierontwerpen</span><span class="sxs-lookup"><span data-stu-id="cfb7f-103">Switch between vendor designs</span></span>

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a><span data-ttu-id="cfb7f-104">Leveranciersgegevensstroom</span><span class="sxs-lookup"><span data-stu-id="cfb7f-104">Vendor data flow</span></span> 

<span data-ttu-id="cfb7f-105">Als u andere Dynamics 365-apps wilt gebruiken voor leveranciersbeheer en u leveranciergegevens wilt isoleren van klanten, kunt u dit elementaire leveranciersontwerp gebruiken.</span><span class="sxs-lookup"><span data-stu-id="cfb7f-105">If you use other Dynamics 365 apps for vendor mastering and you want to isolate vendor information from customers, use this basic vendor design.</span></span>  

![Basisleveranciersstroom](media/dual-write-vendor-data-flow.png)
 
<span data-ttu-id="cfb7f-107">Als u andere Dynamics 365-apps wilt gebruiken voor leveranciersbeheer en u de entiteit **Account** wilt blijven gebruiken voor het opslaan van leveranciergegevens, kunt u dit uitgebreide leveranciersontwerp gebruiken.</span><span class="sxs-lookup"><span data-stu-id="cfb7f-107">If you use other Dynamics 365 apps for vendor mastering and you want to continue to use the **Account** entity for storing vendor information, use this extended vendor design.</span></span> <span data-ttu-id="cfb7f-108">In dit ontwerp wordt uitgebreide leveranciersinformatie, zoals de status in wachtstand voor leveranciers en het leveranciersprofiel opgeslagen in de entiteit **leveranciers** in Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="cfb7f-108">In this design, extended vendor information like vendor on-hold status and vendor profile is stored in the **vendors** entity in Common Data Service.</span></span> 

![Uitgebreide leveranciersstroom](media/dual-write-vendor-detail.jpg)
 
<span data-ttu-id="cfb7f-110">Volg de onderstaande stappen om het uitgebreide leveranciersontwerp te gebruiken:</span><span class="sxs-lookup"><span data-stu-id="cfb7f-110">Follow the below steps to use the extended vendor design:</span></span> 
 
1. <span data-ttu-id="cfb7f-111">Het oplossingspakket **SupplyChainCommon** bevat de sjablonen voor het workflowproces zoals wordt weergegeven in de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="cfb7f-111">The **SupplyChainCommon** solution package contains the workflow process templates as shown in the following image.</span></span>
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="cfb7f-112">![Workflowprocessjablonen](media/dual-write-switch-3.png)</span><span class="sxs-lookup"><span data-stu-id="cfb7f-112">![Workflow process templates](media/dual-write-switch-3.png)</span></span>
2. <span data-ttu-id="cfb7f-113">Maak nieuwe workflowprocessen met de workflowprocessjablonen:</span><span class="sxs-lookup"><span data-stu-id="cfb7f-113">Create new workflow processes using the workflow process templates:</span></span> 
    1. <span data-ttu-id="cfb7f-114">Maak een nieuw workflowproces voor de entiteit **Leverancier** met de workflowprocessjabloon **Leveranciers maken in entiteit Account** en klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="cfb7f-114">Create a new workflow process for the **Vendor** entity using the **Create Vendors in Account Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="cfb7f-115">Deze workflow verwerkt het scenario voor het maken van de entiteit **Account**.</span><span class="sxs-lookup"><span data-stu-id="cfb7f-115">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="cfb7f-116">![Leveranciers maken in entiteit Account](media/dual-write-switch-4.png)</span><span class="sxs-lookup"><span data-stu-id="cfb7f-116">![Create Vendors in Account Entity](media/dual-write-switch-4.png)</span></span>
    2. <span data-ttu-id="cfb7f-117">Maak een nieuw workflowproces voor de entiteit **Leverancier** met de workflowprocessjabloon **Entiteit Accounts bijwerken** en klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="cfb7f-117">Create a new workflow process for the **Vendor** entity using the **Update Accounts Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="cfb7f-118">Deze workflow verwerkt het scenario voor het bijwerken van de entiteit **Account**.</span><span class="sxs-lookup"><span data-stu-id="cfb7f-118">This workflow handles the vendor update scenario for the **Account** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="cfb7f-119">![Entiteit Accounts bijwerken](media/dual-write-switch-5.png)</span><span class="sxs-lookup"><span data-stu-id="cfb7f-119">![Update Accounts Entity](media/dual-write-switch-5.png)</span></span>
    3. <span data-ttu-id="cfb7f-120">Nieuwe workflowprocessen maken op basis van de sjablonen die zijn gemaakt voor de entiteit **Accounts**.</span><span class="sxs-lookup"><span data-stu-id="cfb7f-120">Create new workflow processes from the templates created on the **Accounts** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="cfb7f-121">![Leveranciers maken in entiteit Leveranciers](media/dual-write-switch-6.png)
        > </span><span class="sxs-lookup"><span data-stu-id="cfb7f-121">![Create vendors in vendors entity](media/dual-write-switch-6.png)
        > </span></span>[!div class="mx-imgBorder"]
<span data-ttu-id="cfb7f-122">![Entiteit Leveranciers bijwerken](media/dual-write-switch-7.png)</span><span class="sxs-lookup"><span data-stu-id="cfb7f-122">![Update vendors entity](media/dual-write-switch-7.png)</span></span>
    4. <span data-ttu-id="cfb7f-123">U kunt de workflows configureren als realtime workflows of workflows op de achtergrond op basis van uw vereisten.</span><span class="sxs-lookup"><span data-stu-id="cfb7f-123">You can configure the workflows as real-time or background workflows based on your requirements.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="cfb7f-124">![Converteren naar een workflow op de achtergrond](media/dual-write-switch-8.png)</span><span class="sxs-lookup"><span data-stu-id="cfb7f-124">![Convert to a background workflow](media/dual-write-switch-8.png)</span></span>
    5. <span data-ttu-id="cfb7f-125">Activeer de workflows die u hebt gemaakt voor de entiteiten **Account** en **Leverancier** om te beginnen met het gebruiken van de entiteit **Account** voor het opslaan van leveranciersgegevens.</span><span class="sxs-lookup"><span data-stu-id="cfb7f-125">Activate the workflows that you created on the **Account** and **Vendor** entities to start using the **Account** entity for storing vendor information.</span></span> 
 
