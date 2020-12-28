---
title: Taakbegeleiders opslaan in LCS en opnieuw afspelen
description: In dit artikel wordt uitgelegd hoe u taakbegeleiders opslaat in Microsoft Dynamics Lifecycle Services (LCS) en ze vervolgens opnieuw afspeelt.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b55937c0867117809471f50f1987f7bf12a4b25d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 10/13/2020
ms.locfileid: "4417987"
---
# <a name="save-task-guides-to-lcs-and-replay-them"></a><span data-ttu-id="127e4-103">Taakbegeleiders opslaan in LCS en opnieuw afspelen</span><span class="sxs-lookup"><span data-stu-id="127e4-103">Save task guides to LCS and replay them</span></span>

<span data-ttu-id="127e4-104">**Omgevingsdetails**</span><span class="sxs-lookup"><span data-stu-id="127e4-104">**Environment details**</span></span> 

<span data-ttu-id="127e4-105">Microsoft Dynamics 365 Human Resources is geïmplementeerd via Microsoft Dynamics Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="127e4-105">Microsoft Dynamics 365 Human Resources, which was deployed via Microsoft Dynamics Lifecycle Services (LCS)</span></span>

<span data-ttu-id="127e4-106">**Probleem**</span><span class="sxs-lookup"><span data-stu-id="127e4-106">**Issue**</span></span>

<span data-ttu-id="127e4-107">De klant wil nieuwe taakregistraties in zijn of haar LCS-project opslaan en de opgeslagen taakbegeleiders vervolgens opnieuw afspelen.</span><span class="sxs-lookup"><span data-stu-id="127e4-107">The customer wants to save new task recordings to his or her LCS project, and then replay the saved task guides.</span></span>

<span data-ttu-id="127e4-108">**Resolutie**</span><span class="sxs-lookup"><span data-stu-id="127e4-108">**Resolution**</span></span>

<span data-ttu-id="127e4-109">Ga als volgt te werk om een taakregistratie in LCS op te slaan.</span><span class="sxs-lookup"><span data-stu-id="127e4-109">Follow these steps to save a task recording to LCS.</span></span>

1. <span data-ttu-id="127e4-110">Meld u aan bij LCS en selecteer het project.</span><span class="sxs-lookup"><span data-stu-id="127e4-110">Sign in to LCS, and select the project.</span></span>
2. <span data-ttu-id="127e4-111">Selecteer de tegel **Modelleertool bedrijfsprocessen**.</span><span class="sxs-lookup"><span data-stu-id="127e4-111">Select the **Business process modeler** tile.</span></span>
3. <span data-ttu-id="127e4-112">Geef de pagina weer in de bijgewerkte BPM-ervaring.</span><span class="sxs-lookup"><span data-stu-id="127e4-112">View the page in the "Updated BPM experience."</span></span>
4. <span data-ttu-id="127e4-113">Selecteer een bibliotheek en selecteer **Kopiëren**.</span><span class="sxs-lookup"><span data-stu-id="127e4-113">Select a library, and then select **Copy**.</span></span>
5. <span data-ttu-id="127e4-114">Voer een naam in voor het model van de modelleertool voor bedrijfsprocessen.</span><span class="sxs-lookup"><span data-stu-id="127e4-114">Enter a name for the Business process modeler (BPM) model.</span></span>
6. <span data-ttu-id="127e4-115">Meld u aan bij Human resources vanuit LCS.</span><span class="sxs-lookup"><span data-stu-id="127e4-115">Sign in to Human Resources from LCS.</span></span>
7. <span data-ttu-id="127e4-116">Voer in het veld **Zoeken** het woord **help** in.</span><span class="sxs-lookup"><span data-stu-id="127e4-116">In the **Search** field, enter **help**.</span></span> <span data-ttu-id="127e4-117">De Help van Lifecycle Services wordt geopend.</span><span class="sxs-lookup"><span data-stu-id="127e4-117">Lifecycle Services Help is opened.</span></span>
8. <span data-ttu-id="127e4-118">Selecteer de knop **Vernieuwen** voor Help-configuratie van Lifecycle Services.</span><span class="sxs-lookup"><span data-stu-id="127e4-118">Select the **Refresh** button for Lifecycle Services Help configuration.</span></span>

    <span data-ttu-id="127e4-119">Uw nieuwe BPM-bibliotheek wordt weergegeven en is actief.</span><span class="sxs-lookup"><span data-stu-id="127e4-119">Your new BPM library should appear, and it should be active.</span></span>

9. <span data-ttu-id="127e4-120">Sluit de pagina.</span><span class="sxs-lookup"><span data-stu-id="127e4-120">Close the page.</span></span>
10. <span data-ttu-id="127e4-121">Maak een taakregistratie.</span><span class="sxs-lookup"><span data-stu-id="127e4-121">Create a task recording.</span></span>
11. <span data-ttu-id="127e4-122">Wanneer u klaar bent, selecteert u **Opslaan in Lifecycle Services**.</span><span class="sxs-lookup"><span data-stu-id="127e4-122">When you've finished, select **Save to Lifecycle Services**.</span></span>

    ![Opslaan in Lifecycle Services](media/task-guides.png)

12. <span data-ttu-id="127e4-124">Selecteer de BPM-bibliotheek en het knooppunt waarin u de taakregistratie wilt opslaan.</span><span class="sxs-lookup"><span data-stu-id="127e4-124">Select the BPM library and node to save the task recording to.</span></span>

<span data-ttu-id="127e4-125">Ga als volgt te werk om een taakbegeleider opnieuw af te spelen vanuit LCS.</span><span class="sxs-lookup"><span data-stu-id="127e4-125">Follow these steps to replay a task guide from LCS.</span></span>

1. <span data-ttu-id="127e4-126">Start Taakregistratie.</span><span class="sxs-lookup"><span data-stu-id="127e4-126">Start Task recorder.</span></span>
2. <span data-ttu-id="127e4-127">Selecteer **Openen vanuit LCS**.</span><span class="sxs-lookup"><span data-stu-id="127e4-127">Select **Open from LCS**.</span></span>
3. <span data-ttu-id="127e4-128">Selecteer de bibliotheek en het BPM-knooppunt met de opgeslagen taakbegeleider.</span><span class="sxs-lookup"><span data-stu-id="127e4-128">Select the library and the BPM node that have the saved task guide.</span></span>
4. <span data-ttu-id="127e4-129">Open de taakbegeleider.</span><span class="sxs-lookup"><span data-stu-id="127e4-129">Open the task guide.</span></span>
