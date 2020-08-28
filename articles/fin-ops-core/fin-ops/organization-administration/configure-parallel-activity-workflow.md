---
title: Parallelle activiteiten in een workflow configureren
description: Voer de volgende procedures uit in de workfloweditor om een parallelle activiteit te configureren.
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 998ee559a092c4acd34a6df05e893bdbf4289099
ms.sourcegitcommit: e55efd2f62bf60f678108c09ad4701a76b20cc68
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 08/17/2020
ms.locfileid: "3698310"
---
# <a name="configure-parallel-activities-in-a-workflow"></a><span data-ttu-id="1ae4b-103">Parallelle activiteiten in een workflow configureren</span><span class="sxs-lookup"><span data-stu-id="1ae4b-103">Configure parallel activities in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1ae4b-104">Voer de volgende procedures uit in de workfloweditor om een parallelle activiteit te configureren.</span><span class="sxs-lookup"><span data-stu-id="1ae4b-104">To configure a parallel activity, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="1ae4b-105">Een parallelle activiteit bestaat uit workflowvertakkingen die op hetzelfde moment worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="1ae4b-105">A parallel activity consists of workflow branches that run at the same time.</span></span>

## <a name="name-a-parallel-activity"></a><span data-ttu-id="1ae4b-106">Een parallelle activiteit een naam geven</span><span class="sxs-lookup"><span data-stu-id="1ae4b-106">Name a parallel activity</span></span>

<span data-ttu-id="1ae4b-107">Voer deze stappen uit om een naam op te geven voor een parallelle activiteit.</span><span class="sxs-lookup"><span data-stu-id="1ae4b-107">Follow these steps to enter a name for a parallel activity.</span></span>

1. <span data-ttu-id="1ae4b-108">Klik met de rechtermuisknop op de parallelle activiteit en klik op **Eigenschappen** om het formulier **Eigenschappen** te openen.</span><span class="sxs-lookup"><span data-stu-id="1ae4b-108">Right-click the parallel activity, and then click **Properties** to open the **Properties** form.</span></span>
2. <span data-ttu-id="1ae4b-109">Klik in het linkerdeelvenster op **Basisinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="1ae4b-109">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="1ae4b-110">Voer in het veld **Naam** een unieke naam voor de parallelle activiteit in.</span><span class="sxs-lookup"><span data-stu-id="1ae4b-110">In the **Name** field, enter a unique name for the parallel activity.</span></span>
4. <span data-ttu-id="1ae4b-111">Klik op **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="1ae4b-111">Click **Close**.</span></span>

## <a name="configure-the-branches-of-a-parallel-activity"></a><span data-ttu-id="1ae4b-112">De takken van een parallelle activiteit configureren</span><span class="sxs-lookup"><span data-stu-id="1ae4b-112">Configure the branches of a parallel activity</span></span>

<span data-ttu-id="1ae4b-113">Voer deze stappen uit om de vertakkingen van deze parallelle activiteit toe te voegen en te configureren.</span><span class="sxs-lookup"><span data-stu-id="1ae4b-113">Follow these steps to add and configure the branches of this parallel activity.</span></span>

1. <span data-ttu-id="1ae4b-114">Dubbelklik op de parallelle activiteit om de vertakkingen van de parallelle activiteit weer te geven.</span><span class="sxs-lookup"><span data-stu-id="1ae4b-114">Double-click the parallel activity to display the branches of the parallel activity.</span></span>
2. <span data-ttu-id="1ae4b-115">Om een vertakking toe te voegen, sleept u het element **Vertakking** van het gebied **Workflowelementen** naar een invoegpunt op het tekenpapier.</span><span class="sxs-lookup"><span data-stu-id="1ae4b-115">To add a branch, drag the **Branch** element from the **Workflow elements** area to an insertion point on the canvas.</span></span> <span data-ttu-id="1ae4b-116">De figuur hieronder geeft een invoegpunt weer.</span><span class="sxs-lookup"><span data-stu-id="1ae4b-116">The following figure shows an insertion point.</span></span>

    ![Invoegpunt](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > <span data-ttu-id="1ae4b-118">De volgorde van de vertakkingen is niet belangrijk, omdat alle vertakkingen van een parallelle activiteit op hetzelfde moment worden uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="1ae4b-118">The order of the branches is not important because all the branches of a parallel activity run at the same time.</span></span>

3. <span data-ttu-id="1ae4b-119">Zie [Parallelle vertakkingen in een workflow configureren](configure-parallel-branch-workflow.md) voor configureren van elke vertakking.</span><span class="sxs-lookup"><span data-stu-id="1ae4b-119">To configure each branch, see [Configure parallel branches in a workflow](configure-parallel-branch-workflow.md).</span></span>
