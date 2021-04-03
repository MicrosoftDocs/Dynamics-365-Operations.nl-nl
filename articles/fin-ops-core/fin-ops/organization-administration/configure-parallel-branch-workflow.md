---
title: Parallelle vertakkingen in een workflow configureren
description: Voer de volgende procedures uit in de workfloweditor om een parallelle vertakking te configureren.
author: ChrisGarty
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 196043
ms.assetid: dfdae2b8-6a4f-4760-b339-b755c66f3f89
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 37c177e8c4c4e40bd81287430d9ee7598cf917d8
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566986"
---
# <a name="configure-parallel-branches-in-a-workflow"></a><span data-ttu-id="0f1f2-103">Parallelle vertakkingen in een workflow configureren</span><span class="sxs-lookup"><span data-stu-id="0f1f2-103">Configure parallel branches in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0f1f2-104">Voer de volgende procedures uit in de workfloweditor om een parallelle vertakking te configureren.</span><span class="sxs-lookup"><span data-stu-id="0f1f2-104">To configure a parallel branch, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="0f1f2-105">Een parallelle vertakking is in wezen een workflow die in de context van een bovenliggende workflow wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="0f1f2-105">A parallel branch is essentially a workflow that runs in the context of a parent workflow.</span></span>

## <a name="name-a-branch"></a><span data-ttu-id="0f1f2-106">Een naam opgeven voor een vertakking</span><span class="sxs-lookup"><span data-stu-id="0f1f2-106">Name a branch</span></span>

<span data-ttu-id="0f1f2-107">Voer deze stappen uit om een naam op te geven voor een parallelle vertakking.</span><span class="sxs-lookup"><span data-stu-id="0f1f2-107">Follow these steps to enter a name for a parallel branch.</span></span>

1. <span data-ttu-id="0f1f2-108">Klik met de rechtermuisknop op de parallelle vertakking en klik vervolgens op **Eigenschappen**.</span><span class="sxs-lookup"><span data-stu-id="0f1f2-108">Right-click the parallel branch, and then click **Properties**.</span></span> <span data-ttu-id="0f1f2-109">Het formulier **Eigenschappen** wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="0f1f2-109">The **Properties** form is displayed.</span></span>
2. <span data-ttu-id="0f1f2-110">Klik in het linkerdeelvenster op **Basisinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="0f1f2-110">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="0f1f2-111">Voer in het veld **Naam** een unieke naam voor de parallelle vertakking in.</span><span class="sxs-lookup"><span data-stu-id="0f1f2-111">In the **Name** field, enter a unique name for the parallel branch.</span></span>
4. <span data-ttu-id="0f1f2-112">Klik op **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="0f1f2-112">Click **Close**.</span></span>

## <a name="design-and-configure-the-elements-of-a-branch"></a><span data-ttu-id="0f1f2-113">De elementen van een vertakking ontwerpen en configureren</span><span class="sxs-lookup"><span data-stu-id="0f1f2-113">Design and configure the elements of a branch</span></span>

<span data-ttu-id="0f1f2-114">Voer deze stappen uit om de elementen van een parallelle vertakking te ontwerpen en te configureren.</span><span class="sxs-lookup"><span data-stu-id="0f1f2-114">Follow these steps to design and configure the elements of a parallel branch.</span></span>

1. <span data-ttu-id="0f1f2-115">Dubbelklik op de parallelle vertakking.</span><span class="sxs-lookup"><span data-stu-id="0f1f2-115">Double-click the parallel branch.</span></span>
2. <span data-ttu-id="0f1f2-116">Sleep workflowelementen op het tekenpapier en configureer de elementen, net als bij het maken van een andere workflow.</span><span class="sxs-lookup"><span data-stu-id="0f1f2-116">Drag workflow elements onto the canvas, and then configure the elements, just as you would to create any other workflow.</span></span> <span data-ttu-id="0f1f2-117">Zie [Overzicht van Workflows maken](create-workflow.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="0f1f2-117">For more information, see [Create workflows overview](create-workflow.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0f1f2-118">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="0f1f2-118">Additional resources</span></span>

[<span data-ttu-id="0f1f2-119">Overzicht van Workflows maken</span><span class="sxs-lookup"><span data-stu-id="0f1f2-119">Create workflows overview</span></span>](create-workflow.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]