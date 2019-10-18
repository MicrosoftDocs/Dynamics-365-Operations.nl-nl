---
title: Werkorders en vaste activa
description: In dit onderwerp vindt u meer informatie over werkorders en vaste activa in Activabeheer.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 95fe394d22f9fe81511c230a2cf7b8ddf00d896f
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250824"
---
# <a name="work-orders-and-fixed-assets"></a><span data-ttu-id="a3699-103">Werkorders en vaste activa</span><span class="sxs-lookup"><span data-stu-id="a3699-103">Work orders and fixed assets</span></span>


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="a3699-104">In Activabeheer kunnen activa worden gekoppeld aan vaste activa en kunt u werkorders voor deze activa maken.</span><span class="sxs-lookup"><span data-stu-id="a3699-104">In Asset Management, assets can be related to fixed assets, and you can create work orders for those assets.</span></span> <span data-ttu-id="a3699-105">Als u deze functionaliteit gebruikt, kunt u een volledig overzicht krijgen van vaste activa, gerelateerde investeringsprojecten en de kosten die voor de investeringsprojecten zijn geregistreerd in de module **Projectbeheer en boekhouding** en de module **Vaste activa**.</span><span class="sxs-lookup"><span data-stu-id="a3699-105">If you use this functionality, you can get a complete overview of fixed assets, related investment projects, and the costs registered on the investment projects in the **Project management and accounting** module and the **Fixed assets** module.</span></span>

>[!NOTE]
><span data-ttu-id="a3699-106">Het veld **Vaste-activanummer** wordt alleen ingevuld in het project van de werkordertaak als het projecttype 'Investering' is geselecteerd in het project van de werkordertaak.</span><span class="sxs-lookup"><span data-stu-id="a3699-106">The **Fixed asset number** field is only filled out on the work order job project if type "Investment" is selected as the project type on the work order job project.</span></span>

![Figuur 1](media/24-work-orders.png)

<span data-ttu-id="a3699-108">De volgende procedure beschrijft de relatie tussen activa, werkorders, projecten van werkorderprojecttaken, en vaste activa.</span><span class="sxs-lookup"><span data-stu-id="a3699-108">The following procedure describes the relation between assets, work orders, work order job projects, and fixed assets.</span></span>

1. <span data-ttu-id="a3699-109">U maakt een activum dat u wilt relateren aan vaste activa, zoals in de volgende afbeelding wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="a3699-109">You create an asset that you relate to a fixed asset, as shown in the figure below.</span></span>

![Figuur 2](media/25-work-orders.png)

2. <span data-ttu-id="a3699-111">Wanneer u werkordertypen instelt (**Activabeheer** > **Instellen** > **Werkorders** > **Werkordertypen**), maakt u een werkordertype voor de afhandeling van investeringen.</span><span class="sxs-lookup"><span data-stu-id="a3699-111">When you set up work order types (**Asset management** > **Setup** > **Work orders** > **Work order types**), you create a work order type for handling investments.</span></span> <span data-ttu-id="a3699-112">Zie ook [Werkordertypen](../setup-for-work-orders/work-order-types.md).</span><span class="sxs-lookup"><span data-stu-id="a3699-112">See also [Work order types](../setup-for-work-orders/work-order-types.md).</span></span>

![Figuur 3](media/26-work-orders.png)

3. <span data-ttu-id="a3699-114">Wanneer u werkorderprojectgroepen instelt (koppeling **Activabeheer** > **Instellen** > **Werkorders** > **Projectinstellingen** > **Projectgroep**), maakt u een relatie tussen het werkorder type dat wordt gebruikt voor investeringen en de projectgroep die voor investeringen is gemaakt in de module **Projectbeheer en boekhouding** (**Projectbeheer en boekhouding** > **Instellen** > **Boeking** > **Projectgroepen**).</span><span class="sxs-lookup"><span data-stu-id="a3699-114">When you set up work order project groups (**Asset management** > **Setup** > **Work orders** > **Project setup** > **Project group** link), you create a relation between the work order type used for investments and the project group created for investments in the **Project management and accounting** module (**Project management and accounting** > **Setup** > **Posting** > **Project groups**).</span></span>

![Figuur 4](media/27-work-orders.png)

4. <span data-ttu-id="a3699-116">Wanneer u een werkorder maakt die betrekking heeft op een vaste-activaobject, selecteert u het werkordertype dat voor de afhandeling van investeringen wordt gebruikt, bijvoorbeeld 'Investering'.</span><span class="sxs-lookup"><span data-stu-id="a3699-116">When you create a work order that relates to a fixed asset object, you select the work order type used for handling investments, for example, "Investment".</span></span>

5. <span data-ttu-id="a3699-117">Wanneer de werkorder wordt gemaakt, wordt het bijbehorende werkordertype weergegeven in **Alle werkorders**.</span><span class="sxs-lookup"><span data-stu-id="a3699-117">When the work order is created, the related work order type is shown in **All work orders**.</span></span>

![Figuur 5](media/28-work-orders.png)

6. <span data-ttu-id="a3699-119">Wanneer de werkorder wordt gemaakt, wordt het project dat aan de werkorder is gerelateerd, gemaakt in **Projectbeheer en boekhouding** > **Alle projecten**.</span><span class="sxs-lookup"><span data-stu-id="a3699-119">When the work order is created, the project related to the work order is created in **Project management and accounting** > **All projects**.</span></span> <span data-ttu-id="a3699-120">U kunt projectgerelateerde informatie bekijken door in de werkorder op de koppeling **Project-id** te klikken (open in **Activabeheer** de werkorder in de Detailweergave > sneltabblad **Regeldetails** > tabblad **Algemeen** > veld **Project-id**).</span><span class="sxs-lookup"><span data-stu-id="a3699-120">You can see project-related information by clicking the **Project ID** link on the work order (in **Asset management**, open the work order in Details view > **Line details** FastTab > **General** tab > **Project ID** field).</span></span>

![Figuur 6](media/29-work-orders.png)

7. <span data-ttu-id="a3699-122">In **Vaste activa** kunt u een overzicht bekijken van de projecten die zijn gekoppeld aan vaste activa (**Vaste activa** > **Vaste activa** > **Vaste activa** > klik op het vaste activum in het veld **Vaste-activanummer** > bekijk de inhoud in het deelvenster **Gerelateerde informatie** >sectie **Gekoppelde projecten**).</span><span class="sxs-lookup"><span data-stu-id="a3699-122">In **Fixed assets**, you are able to see an overview of the projects associated with a fixed asset (**Fixed assets** > **Fixed assets** > **Fixed assets** > click on the fixed asset in the **Fixed asset number** field > view the contents in the **Related information** pane > **Associated projects** section).</span></span>

