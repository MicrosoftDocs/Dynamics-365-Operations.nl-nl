---
title: Werkorders en vaste activa
description: In dit onderwerp vindt u meer informatie over werkorders en vaste activa in Activabeheer.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ca7a5d88de4308d7be9c1bc749b9dbf1da027c2c
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 04/02/2020
ms.locfileid: "3208818"
---
# <a name="work-orders-and-fixed-assets"></a><span data-ttu-id="068ff-103">Werkorders en vaste activa</span><span class="sxs-lookup"><span data-stu-id="068ff-103">Work orders and fixed assets</span></span>

[!include [banner](../../includes/banner.md)]


<span data-ttu-id="068ff-104">In Activabeheer kunnen activa worden gekoppeld aan vaste activa en kunt u werkorders voor deze activa maken.</span><span class="sxs-lookup"><span data-stu-id="068ff-104">In Asset Management, assets can be related to fixed assets, and you can create work orders for those assets.</span></span> <span data-ttu-id="068ff-105">Als u deze functionaliteit gebruikt, kunt u een volledig overzicht krijgen van vaste activa, gerelateerde investeringsprojecten en de kosten die voor de investeringsprojecten zijn geregistreerd in de modules **Projectbeheer en boekhouding** en **Vaste activa** in Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="068ff-105">If you use this functionality, you can get a complete overview of fixed assets, related investment projects, and the costs that are registered on the investment projects in the **Project management and accounting** and **Fixed assets** modules in Microsoft Dynamics 365 for Finance and Operations.</span></span>

>[!NOTE]
><span data-ttu-id="068ff-106">Het veld **Vaste-activanummer** in het project van de werkordertaak wordt alleen ingesteld als het projecttype **Investering** is geselecteerd in het project van de werkordertaak.</span><span class="sxs-lookup"><span data-stu-id="068ff-106">The **Fixed asset number** field on the work order job project is set only if **Investment** is selected as the project type on the work order job project.</span></span>

<span data-ttu-id="068ff-107">In de onderstaande afbeelding ziet u de relatie tussen een investeringsproject in de module **Projectbeheer en boekhouding** en het project van een werkorder.</span><span class="sxs-lookup"><span data-stu-id="068ff-107">The illustration below shows the relation between an investment project in the **Project management and accounting** module and a work order job project.</span></span>

![Figuur 1](media/24-work-orders.png)

<span data-ttu-id="068ff-109">De volgende procedure beschrijft de relatie tussen activa, werkorders, projecten van werkorderprojecttaken, en vaste activa.</span><span class="sxs-lookup"><span data-stu-id="068ff-109">The following procedure describes the relation between assets, work orders, work order job projects, and fixed assets.</span></span>

1. <span data-ttu-id="068ff-110">U maakt een activum dat u aan een vast activum relateert.</span><span class="sxs-lookup"><span data-stu-id="068ff-110">You create an asset that you relate to a fixed asset.</span></span>

![Figuur 2](media/25-work-orders.png)

2. <span data-ttu-id="068ff-112">Wanneer u werkordertypen op de pagina **Werkordertypen** instelt (**Activabeheer** > **Instellen** > **Werkorders** > **Werkordertypen**), maakt u een werkordertype voor de afhandeling van investeringen.</span><span class="sxs-lookup"><span data-stu-id="068ff-112">When you set up work order types on the **Work order types** page (**Asset management** > **Setup** > **Work orders** > **Work order types**), you create a work order type for handling investments.</span></span> <span data-ttu-id="068ff-113">Zie ook [Werkordertypen](../setup-for-work-orders/work-order-types.md).</span><span class="sxs-lookup"><span data-stu-id="068ff-113">See also [Work order types](../setup-for-work-orders/work-order-types.md).</span></span>

![Figuur 3](media/26-work-orders.png)

3. <span data-ttu-id="068ff-115">Wanneer u werkorderprojectgroepen op het tabblad **Projectgroep** van de pagina **Projectinstellingen werkorder** instelt (**Activabeheer** > **Instellen** > **Werkorders** > **Projectinstellingen**Projectgroep), maakt u een relatie tussen het werkordertype dat wordt gebruikt voor investeringen en de projectgroep die voor investeringen is gemaakt op de pagina **Projectgroepen** van de module **Projectbeheer en boekhouding** (**Projectbeheer en boekhouding** > **Instellen** > **Boeking** > **Projectgroepen**).</span><span class="sxs-lookup"><span data-stu-id="068ff-115">When you set up work order project groups on the **Project group** tab of the **Work order project setup** page (**Asset management** > **Setup** > **Work orders** > **Project setup**), you create a relation between the work order type that is used for investments and the project group that was created for investments on the **Project groups** page in the **Project management and accounting** module (**Project management and accounting** > **Setup** > **Posting** > **Project groups**).</span></span>

![Figuur 4](media/27-work-orders.png)

4. <span data-ttu-id="068ff-117">Wanneer u een werkorder maakt die betrekking heeft op een vast activum, selecteert u het werkordertype dat wordt gebruikt voor de afhandeling van investeringen, bijvoorbeeld **Investering**.</span><span class="sxs-lookup"><span data-stu-id="068ff-117">When you create a work order that is related to a fixed asset, you select the work order type that is used to handle investments, such as **Investment**.</span></span>

5. <span data-ttu-id="068ff-118">Wanneer de werkorder is gemaakt, wordt het bijbehorende werkordertype weergegeven op de pagina **Alle werkorders**.</span><span class="sxs-lookup"><span data-stu-id="068ff-118">When the work order is created, the related work order type is shown on the **All work orders** page.</span></span>

![Figuur 5](media/28-work-orders.png)

6. <span data-ttu-id="068ff-120">Wanneer de werkorder is gemaakt, wordt het project dat aan de werkorder is gekoppeld, gemaakt op de pagina **Alle projecten** van de module **Projectbeheer en boekhouding** (**Projectbeheer en boekhouding** > **Projecten** > **Alle projecten**).</span><span class="sxs-lookup"><span data-stu-id="068ff-120">When the work order is created, the project that is related to the work order is created on the **All projects** page in the **Project management and accounting** module (**Project management and accounting** > **Projects** > **All projects**).</span></span> <span data-ttu-id="068ff-121">Als u projectgerelateerde informatie wilt bekijken, selecteert u de koppeling in het veld **Project-id** op het tabblad **Algemeen** van het sneltabblad **Regeldetails** in de detailweergave van de pagina **Alle werkorders** van de module **Activabeheer** (**Activabeheer** > **Algemeen** > **Werkorders** > **Alle werkorders**).</span><span class="sxs-lookup"><span data-stu-id="068ff-121">To view project-related information, select the link in the **Project ID** field on the **General** tab on the **Line details** FastTab in the details view of the **All work orders** page in the **Asset management** module (**Asset management** > **Commom** > **Work orders** > **All work orders**).</span></span>

![Figuur 6](media/29-work-orders.png)

7. <span data-ttu-id="068ff-123">Als u een overzicht wilt weergeven van de projecten die aan een vast activum zijn gekoppeld, selecteert u **Vaste activa** > **Vaste activa** > **Vaste activa** en selecteert u vervolgens in het veld **Vaste-activanummer** de koppeling naar het vaste activum om de detailweergave te openen.</span><span class="sxs-lookup"><span data-stu-id="068ff-123">To see an overview of the projects associated with a fixed asset, select **Fixed assets** > **Fixed assets** > **Fixed assets**, and then, in the **Fixed asset number** field, select the link for the fixed asset to open the details view.</span></span> <span data-ttu-id="068ff-124">Vouw het deelvenster **Gerelateerde informatie**, rechts van de pagina, uit en selecteer het sneltabblad **Gekoppelde projecten**.</span><span class="sxs-lookup"><span data-stu-id="068ff-124">Expand the **Related information** pane on the right side of the page, and select the **Associated projects** FastTab.</span></span>

