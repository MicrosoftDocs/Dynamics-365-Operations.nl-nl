---
title: Schakelen tussen leveranciersontwerpen
description: ''
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
ms.openlocfilehash: 4e97ff0b0e6195b5e3703e15a0bb0de7644ef8d1
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772359"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="25dad-102">Schakelen tussen leveranciersontwerpen</span><span class="sxs-lookup"><span data-stu-id="25dad-102">Switch between vendor designs</span></span>

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a><span data-ttu-id="25dad-103">Leveranciersgegevensstroom</span><span class="sxs-lookup"><span data-stu-id="25dad-103">Vendor data flow</span></span> 

<span data-ttu-id="25dad-104">Als u andere Dynamics 365-apps wilt gebruiken voor leveranciersbeheer en u leveranciergegevens wilt isoleren van klanten, kunt u dit elementaire leveranciersontwerp gebruiken.</span><span class="sxs-lookup"><span data-stu-id="25dad-104">If you use other Dynamics 365 apps for vendor mastering and you want to isolate vendor information from customers, use this basic vendor design.</span></span>  

![Basisleveranciersstroom](media/dual-write-switch-1.png)
 
<span data-ttu-id="25dad-106">Als u andere Dynamics 365-apps wilt gebruiken voor leveranciersbeheer en u de entiteit **Account** wilt blijven gebruiken voor het opslaan van leveranciergegevens, kunt u dit uitgebreide leveranciersontwerp gebruiken.</span><span class="sxs-lookup"><span data-stu-id="25dad-106">If you use other Dynamics 365 apps for vendor mastering and you want to continue to use the **Account** entity for storing vendor information, use this extended vendor design.</span></span> <span data-ttu-id="25dad-107">In dit ontwerp wordt uitgebreide leveranciersinformatie, zoals de status in wachtstand voor leveranciers en het leveranciersprofiel opgeslagen in de entiteit **leveranciers** in Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="25dad-107">In this design, extended vendor information like vendor on-hold status and vendor profile is stored in the **vendors** entity in Common Data Service.</span></span> 

![Uitgebreide leveranciersstroom](media/dual-write-switch-2.png)
 
<span data-ttu-id="25dad-109">Volg de onderstaande stappen om het uitgebreide leveranciersontwerp te gebruiken:</span><span class="sxs-lookup"><span data-stu-id="25dad-109">Follow the below steps to use the extended vendor design:</span></span> 
 
1. <span data-ttu-id="25dad-110">Het oplossingspakket **SupplyChainCommon** bevat de sjablonen voor het workflowproces zoals wordt weergegeven in de volgende afbeelding.</span><span class="sxs-lookup"><span data-stu-id="25dad-110">The **SupplyChainCommon** solution package contains the workflow process templates as shown in the following image.</span></span>
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="25dad-111">![Workflowprocessjablonen](media/dual-write-switch-3.png)</span><span class="sxs-lookup"><span data-stu-id="25dad-111">![Workflow process templates](media/dual-write-switch-3.png)</span></span>
2. <span data-ttu-id="25dad-112">Maak nieuwe workflowprocessen met de workflowprocessjablonen:</span><span class="sxs-lookup"><span data-stu-id="25dad-112">Create new workflow processes using the workflow process templates:</span></span> 
    1. <span data-ttu-id="25dad-113">Maak een nieuw workflowproces voor de entiteit **Leverancier** met de workflowprocessjabloon **Leveranciers maken in entiteit Account** en klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="25dad-113">Create a new workflow process for the **Vendor** entity using the **Create Vendors in Account Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="25dad-114">Deze workflow verwerkt het scenario voor het maken van de entiteit **Account**.</span><span class="sxs-lookup"><span data-stu-id="25dad-114">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="25dad-115">![Leveranciers maken in entiteit Account](media/dual-write-switch-4.png)</span><span class="sxs-lookup"><span data-stu-id="25dad-115">![Create Vendors in Account Entity](media/dual-write-switch-4.png)</span></span>
    2. <span data-ttu-id="25dad-116">Maak een nieuw workflowproces voor de entiteit **Leverancier** met de workflowprocessjabloon **Entiteit Accounts bijwerken** en klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="25dad-116">Create a new workflow process for the **Vendor** entity using the **Update Accounts Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="25dad-117">Deze workflow verwerkt het scenario voor het bijwerken van de entiteit **Account**.</span><span class="sxs-lookup"><span data-stu-id="25dad-117">This workflow handles the vendor update scenario for the **Account** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="25dad-118">![Entiteit Accounts bijwerken](media/dual-write-switch-5.png)</span><span class="sxs-lookup"><span data-stu-id="25dad-118">![Update Accounts Entity](media/dual-write-switch-5.png)</span></span>
    3. <span data-ttu-id="25dad-119">Nieuwe workflowprocessen maken op basis van de sjablonen die zijn gemaakt voor de entiteit **Accounts**.</span><span class="sxs-lookup"><span data-stu-id="25dad-119">Create new workflow processes from the templates created on the **Accounts** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="25dad-120">![Leveranciers maken in entiteit Leveranciers](media/dual-write-switch-6.png)
        > </span><span class="sxs-lookup"><span data-stu-id="25dad-120">![Create vendors in vendors entity](media/dual-write-switch-6.png)
        > </span></span>[!div class="mx-imgBorder"]
<span data-ttu-id="25dad-121">![Entiteit Leveranciers bijwerken](media/dual-write-switch-7.png)</span><span class="sxs-lookup"><span data-stu-id="25dad-121">![Update vendors entity](media/dual-write-switch-7.png)</span></span>
    4. <span data-ttu-id="25dad-122">U kunt de workflows configureren als realtime workflows of workflows op de achtergrond op basis van uw vereisten.</span><span class="sxs-lookup"><span data-stu-id="25dad-122">You can configure the workflows as real-time or background workflows based on your requirements.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="25dad-123">![Converteren naar een workflow op de achtergrond](media/dual-write-switch-8.png)</span><span class="sxs-lookup"><span data-stu-id="25dad-123">![Convert to a background workflow](media/dual-write-switch-8.png)</span></span>
    5. <span data-ttu-id="25dad-124">Activeer de workflows die u hebt gemaakt voor de entiteiten **Account** en **Leverancier** om te beginnen met het gebruiken van de entiteit **Account** van Customer Engagement voor het opslaan van leveranciersgegevens.</span><span class="sxs-lookup"><span data-stu-id="25dad-124">Activate the workflows that you created on the **Account** and **Vendor** entities to start using the Customer Engagement **Account** entity for storing vendor information.</span></span> 
 
