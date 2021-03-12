---
title: Een hoofdplanningstaak annuleren
description: In dit onderwerp wordt uitgelegd hoe u een actieve planningstaak kunt annuleren die gebruikmaakt van ingebouwde planningsfunctionaliteit.
author: ChristianRytt
manager: tfehr
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace, ReqProcessList
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-12-16
ms.dyn365.ops.version: ''
ms.openlocfilehash: 40d657a02df0cba66918a6853ec62621501cfdfe
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989788"
---
# <a name="cancel-a-master-planning-job"></a><span data-ttu-id="0bf7e-103">Een hoofdplanningstaak annuleren</span><span class="sxs-lookup"><span data-stu-id="0bf7e-103">Cancel a master planning job</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0bf7e-104">In Microsoft Dynamics 365 Supply Chain Management zijn er meerdere opties voor het annuleren van een hoofdplanningstaak.</span><span class="sxs-lookup"><span data-stu-id="0bf7e-104">In Microsoft Dynamics 365 Supply Chain Management, there are multiple options for canceling a master planning job.</span></span> <span data-ttu-id="0bf7e-105">U kunt bijvoorbeeld een hoofdplanningstaak annuleren als deze per ongeluk is gestart of langer duurt dan verwacht en u deze wilt beëindigen.</span><span class="sxs-lookup"><span data-stu-id="0bf7e-105">For example, you may want to cancel a master planning job if it was started by mistake or is running longer than expected and you want to end it.</span></span> <span data-ttu-id="0bf7e-106">U kunt een planningstaak het beste annuleren via de de pagina **Onvoltooide planningsprocessen**.</span><span class="sxs-lookup"><span data-stu-id="0bf7e-106">The best way to cancel a planning job is from  the **Unfinished planning processes** page.</span></span> <span data-ttu-id="0bf7e-107">Alternatieve opties op de pagina's **Batchtaken** en **Verbeterde batchtaken** mogen alleen worden gebruikt als het annuleren van de hoofdplanningstaak via de pagina **Onvoltooide planningsprocessen** niet binnen enkele minuten is voltooid.</span><span class="sxs-lookup"><span data-stu-id="0bf7e-107">Alternative options from the **Batch jobs** and **Batch jobs enhanced** pages should only be used if canceling the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

## <a name="preferred-cancel-option"></a><span data-ttu-id="0bf7e-108">Voorkeursoptie voor annuleren</span><span class="sxs-lookup"><span data-stu-id="0bf7e-108">Preferred cancel option</span></span>
### <a name="cancel-master-planning-job-from-unfinished-planning-processes-page"></a><span data-ttu-id="0bf7e-109">Hoofdplanningstaak annuleren via de de pagina **Onvoltooide planningsprocessen**</span><span class="sxs-lookup"><span data-stu-id="0bf7e-109">Cancel master planning job from **Unfinished planning processes** page</span></span>
1. <span data-ttu-id="0bf7e-110">Ga naar **Hoofdplanning > Query's en rapporten > Hoofdplanning > Onvoltooide planningsprocessen**.</span><span class="sxs-lookup"><span data-stu-id="0bf7e-110">Go to **Master planning > Inquiries and reports > Master planning > Unfinished planning processes**.</span></span>
2. <span data-ttu-id="0bf7e-111">Selecteer de regel met het planningsproces dat u wilt annuleren.</span><span class="sxs-lookup"><span data-stu-id="0bf7e-111">Select the line with the planning process that you want to cancel.</span></span>
3. <span data-ttu-id="0bf7e-112">Klik op **Annuleren**.</span><span class="sxs-lookup"><span data-stu-id="0bf7e-112">Click **Cancel**.</span></span>

## <a name="additional-cancel-options"></a><span data-ttu-id="0bf7e-113">Overige annuleringsopties</span><span class="sxs-lookup"><span data-stu-id="0bf7e-113">Additional cancel options</span></span>
<span data-ttu-id="0bf7e-114">Deze moeten alleen worden gebruikt als het annuleren van de hoofdplanningstaak via de pagina **Onvoltooide planningsprocessen** niet binnen enkele minuten is voltooid.</span><span class="sxs-lookup"><span data-stu-id="0bf7e-114">These should only be used if canceling the master planning job from the **Unfinished planning processes** page did not complete within a few minutes.</span></span>

### <a name="delete-master-planning-job-from-the-batch-jobs-page"></a><span data-ttu-id="0bf7e-115">Hoofdplanningstaak verwijderen via de pagina **Batchtaken**</span><span class="sxs-lookup"><span data-stu-id="0bf7e-115">Delete master planning job from the **Batch jobs** page</span></span>
1. <span data-ttu-id="0bf7e-116">Ga naar **Systeembeheer > Query's > Batchtaken**.</span><span class="sxs-lookup"><span data-stu-id="0bf7e-116">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="0bf7e-117">Selecteer de regel met de planningstaak die u wilt verwijderen.</span><span class="sxs-lookup"><span data-stu-id="0bf7e-117">Select the line with the planning job that you want to delete.</span></span>
3. <span data-ttu-id="0bf7e-118">Klik op **Verwijderen**.</span><span class="sxs-lookup"><span data-stu-id="0bf7e-118">Click **Delete**.</span></span>

### <a name="abort-master-planning-job-task-from-the-batch-jobs-enhanced-page"></a><span data-ttu-id="0bf7e-119">Hoofdplanningstaak afbreken via de pagina **Verbeterde batchtaken**</span><span class="sxs-lookup"><span data-stu-id="0bf7e-119">Abort master planning job task from the **Batch jobs enhanced** page</span></span>
1. <span data-ttu-id="0bf7e-120">Ga naar **Systeembeheer > Query's > Batchtaken**.</span><span class="sxs-lookup"><span data-stu-id="0bf7e-120">Go to **System administration > Inquiries > Batch jobs**.</span></span>
2. <span data-ttu-id="0bf7e-121">Als de taak-id niet in de lijst wordt weergegeven, klikt u op **Overschakelen naar uitgebreid formulier** of gaat u verder met de volgende stap.</span><span class="sxs-lookup"><span data-stu-id="0bf7e-121">If the job ID is not shown in the list, click **Switch to enhanced form**, otherwise proceed with the next step.</span></span>
3. <span data-ttu-id="0bf7e-122">Open de batchtaak.</span><span class="sxs-lookup"><span data-stu-id="0bf7e-122">Open the batch job.</span></span> <span data-ttu-id="0bf7e-123">Klik op de **taak-id** voor de batchtaak met taken die u wilt beëindigen.</span><span class="sxs-lookup"><span data-stu-id="0bf7e-123">Click the **Job ID** for the batch job with tasks that you want to end.</span></span>
4. <span data-ttu-id="0bf7e-124">Selecteer bij **Batchtaken** de taken die u wilt beëindigen.</span><span class="sxs-lookup"><span data-stu-id="0bf7e-124">In **Batch tasks**, select the tasks to end.</span></span>
5. <span data-ttu-id="0bf7e-125">Klik op **Status wijzigen**, kies **Annuleren** en klik op **OK**.</span><span class="sxs-lookup"><span data-stu-id="0bf7e-125">Click **Change status**, choose **Canceling** and click **OK**.</span></span>
6. <span data-ttu-id="0bf7e-126">Klik op het sneltabblad **Batchtaken** op **Afbreken**.</span><span class="sxs-lookup"><span data-stu-id="0bf7e-126">On the **Batch tasks** FastTab, click **Abort**.</span></span>
