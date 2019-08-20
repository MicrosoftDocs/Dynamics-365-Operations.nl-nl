---
title: Werkorders maken van onderhoudsverzoeken
description: In dit onderwerp wordt uitgelegd hoe u een werkorder van een onderhoudsverzoek maakt in Activabeheer.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
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
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3f7af87f359cfe3a606c8be857dd905bfef75e97
ms.sourcegitcommit: 871b76f8808a48d282f151144829323258ffc912
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/02/2019
ms.locfileid: "1847454"
---
# <a name="create-work-orders-from-maintenance-requests"></a><span data-ttu-id="7c279-103">Werkorders maken van onderhoudsverzoeken</span><span class="sxs-lookup"><span data-stu-id="7c279-103">Create work orders from maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="7c279-104">Wanneer u onderhoudsverzoeken hebt gemaakt, kunt u deze eenvoudig omzetten in werkorders.</span><span class="sxs-lookup"><span data-stu-id="7c279-104">After you've created maintenance requests, you can easily convert them to work orders.</span></span> <span data-ttu-id="7c279-105">In dit onderwerp wordt beschreven hoe u het snelst kunt werken met onderhoudsverzoeken, verschillende onderhoudsverzoeken tegelijk kunt bijwerken en vervolgens een werkorder kunt maken voor meerdere onderhoudsverzoeken tegelijk.</span><span class="sxs-lookup"><span data-stu-id="7c279-105">This topic describes the quickest way to work with maintenance requests, update several maintenance requests at the same time, and then create a work order for several maintenance requests at the same time.</span></span> <span data-ttu-id="7c279-106">Op de pagina **Actieve onderhoudsaanvragen** of **De onderhoudsverzoeken van mijn functionele locatie** kunt u ook met één onderhoudsverzoek tegelijk werken en één onderhoudsverzoek in een werkorder omzetten.</span><span class="sxs-lookup"><span data-stu-id="7c279-106">On the **Active maintenance requests** or **My functional location maintenance requests** page, you can also work with one maintenance request at a time and convert one maintenance request to a work order.</span></span>

> [!NOTE]
> <span data-ttu-id="7c279-107">Elk onderhoudsverzoek kan aan slechts één werkorder worden gekoppeld.</span><span class="sxs-lookup"><span data-stu-id="7c279-107">Every maintenance request can be related to only one work order.</span></span> <span data-ttu-id="7c279-108">Meerdere onderhoudsverzoeken kunnen echter wel in één werkorder worden opgenomen, zelfs als de onderhoudsverzoeken verschillende activa hebben.</span><span class="sxs-lookup"><span data-stu-id="7c279-108">However, multiple maintenance requests can be included in one work order, even if the maintenance requests have different assets.</span></span>

1. <span data-ttu-id="7c279-109">Selecteer **Activabeheer** \> **Algemeen** \> **Onderhoudsaanvragen** \> **Alle onderhoudsverzoeken**.</span><span class="sxs-lookup"><span data-stu-id="7c279-109">Select **Asset management** \> **Common** \> **maintenance requests** \> **All maintenance requests**.</span></span>
2. <span data-ttu-id="7c279-110">Voordat u een werkorder van onderhoudsverzoeken kunt maken, moet u minimaal één type onderhoudstaak selecteren voor de onderhoudsverzoeken, en ook een type onderhoudstaak variant en vakgebied, als deze informatie relevant is.</span><span class="sxs-lookup"><span data-stu-id="7c279-110">Before you can create a work order from maintenance requests, you must select, at a minimum, a maintenance job type for the maintenance requests, and also a maintenance job type variant and trade, if this information is relevant.</span></span> <span data-ttu-id="7c279-111">In de rasterweergave kunt u eenvoudig informatie voor een onderhoudsverzoek bijwerken.</span><span class="sxs-lookup"><span data-stu-id="7c279-111">In the grid view, you can easily update information for a maintenance request.</span></span>
3. <span data-ttu-id="7c279-112">Wanneer u klaar bent om een werkorder te maken, selecteert u de onderhoudsverzoeken die u wilt opnemen.</span><span class="sxs-lookup"><span data-stu-id="7c279-112">When you're ready to create a work order, select the maintenance requests to include in it.</span></span>

    - <span data-ttu-id="7c279-113">Als u meerdere onderhoudsverzoeken selecteert om in een werkorder om te zetten, moeten zowel het veld **Activum** als het veld **Type onderhoudstaak** zijn ingesteld voordat u de werkorder maakt.</span><span class="sxs-lookup"><span data-stu-id="7c279-113">If you select several maintenance requests to convert to a work order, both the **Asset** field and the **Maintenance job type** field must be set before you create the work order.</span></span>
    - <span data-ttu-id="7c279-114">Als u één onderhoudsverzoek selecteert om in een werkorder om te zetten, moet alleen het veld **Activum** worden ingesteld voordat u de werkorder maakt.</span><span class="sxs-lookup"><span data-stu-id="7c279-114">If you select one maintenance request to convert to a work order, only the **Asset** field must be set before you create the work order.</span></span> <span data-ttu-id="7c279-115">Wanneer u echter de werkorder maakt, kunt u een onderhoudstaaktype (en een gerelateerd onderhoudstaaktype variant en vakgebied, als deze informatie relevant is) in het dialoogvenster **Werkorder** selecteren.</span><span class="sxs-lookup"><span data-stu-id="7c279-115">However, when you create the work order, you can select a maintenance job type (and a related maintenance job type variant and trade, if this information is relevant) in the **Create work order** dialog box.</span></span>

4. <span data-ttu-id="7c279-116">Selecteer **Werkorder**.</span><span class="sxs-lookup"><span data-stu-id="7c279-116">Select **Work order**.</span></span>
5. <span data-ttu-id="7c279-117">Stel in het dialoogvenster **Werkorder maken** de velden in en selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="7c279-117">In the **Create work order** dialog box, set the fields, and then select **OK**.</span></span>

    <span data-ttu-id="7c279-118">Op een berichtenbalk kan een bericht verschijnen dat een nieuwe werkorder is gemaakt.</span><span class="sxs-lookup"><span data-stu-id="7c279-118">A message bar might notify you that a new work order has been created.</span></span>

    <span data-ttu-id="7c279-119">Wanneer u een werkorder maakt die is gebaseerd op een onderhoudsverzoek en als het activum dat aan het onderhoudsverzoek is gekoppeld, wordt opgenomen in een garantieovereenkomst, verschijnt er op een berichtenbalk een bericht over de garantieovereenkomst.</span><span class="sxs-lookup"><span data-stu-id="7c279-119">Additionally, when you create a work order that is based on a maintenance request, if the asset that is related to the maintenance request is included in a warranty agreement, a message bar notifies you about the warranty agreement.</span></span>

6. <span data-ttu-id="7c279-120">Selecteer **Activabeheer** \> **Algemeen** \> **Werkorders** \> **Alle werkorders** en open de nieuwe werkorder.</span><span class="sxs-lookup"><span data-stu-id="7c279-120">Select **Asset management** \> **Common** \> **Work orders** \> **All work orders**, and open the new work order.</span></span>

    ![Figuur 1](media/05-manage-maintenance-requests.png)

