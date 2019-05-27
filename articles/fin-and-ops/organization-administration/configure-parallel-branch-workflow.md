---
title: Parallelle vertakkingen in een workflow configureren
description: Voer de volgende procedures uit in de workfloweditor om een parallelle vertakking te configureren.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 196043
ms.assetid: dfdae2b8-6a4f-4760-b339-b755c66f3f89
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 73626ad21dfe2be7400f321a3eee272c896276f3
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 05/15/2019
ms.locfileid: "1570734"
---
# <a name="configure-parallel-branches-in-a-workflow"></a><span data-ttu-id="c3e1b-103">Parallelle vertakkingen in een workflow configureren</span><span class="sxs-lookup"><span data-stu-id="c3e1b-103">Configure parallel branches in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c3e1b-104">Voer de volgende procedures uit in de workfloweditor om een parallelle vertakking te configureren.</span><span class="sxs-lookup"><span data-stu-id="c3e1b-104">To configure a parallel branch, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="c3e1b-105">Een parallelle vertakking is in wezen een workflow die in de context van een bovenliggende workflow wordt uitgevoerd.</span><span class="sxs-lookup"><span data-stu-id="c3e1b-105">A parallel branch is essentially a workflow that runs in the context of a parent workflow.</span></span>

## <a name="name-a-branch"></a><span data-ttu-id="c3e1b-106">Een naam opgeven voor een vertakking</span><span class="sxs-lookup"><span data-stu-id="c3e1b-106">Name a branch</span></span>

<span data-ttu-id="c3e1b-107">Voer deze stappen uit om een naam op te geven voor een parallelle vertakking.</span><span class="sxs-lookup"><span data-stu-id="c3e1b-107">Follow these steps to enter a name for a parallel branch.</span></span>

1. <span data-ttu-id="c3e1b-108">Klik met de rechtermuisknop op de parallelle vertakking en klik vervolgens op **Eigenschappen**.</span><span class="sxs-lookup"><span data-stu-id="c3e1b-108">Right-click the parallel branch, and then click **Properties**.</span></span> <span data-ttu-id="c3e1b-109">Het formulier **Eigenschappen** wordt weergegeven.</span><span class="sxs-lookup"><span data-stu-id="c3e1b-109">The **Properties** form is displayed.</span></span>
2. <span data-ttu-id="c3e1b-110">Klik in het linkerdeelvenster op **Basisinstellingen**.</span><span class="sxs-lookup"><span data-stu-id="c3e1b-110">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="c3e1b-111">Voer in het veld **Naam** een unieke naam voor de parallelle vertakking in.</span><span class="sxs-lookup"><span data-stu-id="c3e1b-111">In the **Name** field, enter a unique name for the parallel branch.</span></span>
4. <span data-ttu-id="c3e1b-112">Klik op **Sluiten**.</span><span class="sxs-lookup"><span data-stu-id="c3e1b-112">Click **Close**.</span></span>

## <a name="design-and-configure-the-elements-of-a-branch"></a><span data-ttu-id="c3e1b-113">De elementen van een vertakking ontwerpen en configureren</span><span class="sxs-lookup"><span data-stu-id="c3e1b-113">Design and configure the elements of a branch</span></span>

<span data-ttu-id="c3e1b-114">Voer deze stappen uit om de elementen van een parallelle vertakking te ontwerpen en te configureren.</span><span class="sxs-lookup"><span data-stu-id="c3e1b-114">Follow these steps to design and configure the elements of a parallel branch.</span></span>

1. <span data-ttu-id="c3e1b-115">Dubbelklik op de parallelle vertakking.</span><span class="sxs-lookup"><span data-stu-id="c3e1b-115">Double-click the parallel branch.</span></span>
2. <span data-ttu-id="c3e1b-116">Sleep workflowelementen op het tekenpapier en configureer de elementen, net als bij het maken van een andere workflow.</span><span class="sxs-lookup"><span data-stu-id="c3e1b-116">Drag workflow elements onto the canvas, and then configure the elements, just as you would to create any other workflow.</span></span> <span data-ttu-id="c3e1b-117">Zie [Een workflow maken](create-workflow.md) voor meer informatie.</span><span class="sxs-lookup"><span data-stu-id="c3e1b-117">For more information, see [Create a workflow](create-workflow.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c3e1b-118">Aanvullende resources</span><span class="sxs-lookup"><span data-stu-id="c3e1b-118">Additional resources</span></span>

[<span data-ttu-id="c3e1b-119">Een workflow maken</span><span class="sxs-lookup"><span data-stu-id="c3e1b-119">Create a workflow</span></span>](create-workflow.md)
