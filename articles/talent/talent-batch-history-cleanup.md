---
title: Prestaties optimaliseren met taken met automatische opschoning
description: In dit onderwerp wordt uitgelegd hoe u enkele prestatie problemen met Microsoft Dynamics 365 Talent kunt oplossen door de batchtaakgeschiedenis op te schonen.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2019-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: 1e9d237817024800ad9880ec58db3505ac1c493f
ms.sourcegitcommit: f87de0f949b5d60993b19e0f61297f02d42b5bef
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 09/24/2019
ms.locfileid: "2027079"
---
# <a name="optimize-performance-with-auto-cleanup-tasks"></a><span data-ttu-id="ef9a4-103">Prestaties optimaliseren met taken met automatische opschoning</span><span class="sxs-lookup"><span data-stu-id="ef9a4-103">Optimize performance with auto cleanup tasks</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ef9a4-104">**Uitgifte**</span><span class="sxs-lookup"><span data-stu-id="ef9a4-104">**Issue**</span></span>

<span data-ttu-id="ef9a4-105">Microsoft Dynamics 365 Talent kan prestatieproblemen ondervinden als de batchtaakgeschiedenis te groot wordt.</span><span class="sxs-lookup"><span data-stu-id="ef9a4-105">Microsoft Dynamics 365 Talent can experience performance issues if the batch job history grows too large.</span></span>

<span data-ttu-id="ef9a4-106">**Oorzaak**</span><span class="sxs-lookup"><span data-stu-id="ef9a4-106">**Cause**</span></span>

<span data-ttu-id="ef9a4-107">Batchtaken die vaak worden uitgevoerd, kunnen leiden tot een onhoudbare groei van de batchtaakgeschiedenis.</span><span class="sxs-lookup"><span data-stu-id="ef9a4-107">Batch jobs that run frequently can lead to unsustainable growth of the batch job history.</span></span> <span data-ttu-id="ef9a4-108">Dit kan prestatieproblemen veroorzaken.</span><span class="sxs-lookup"><span data-stu-id="ef9a4-108">This can cause performance issues.</span></span> 

<span data-ttu-id="ef9a4-109">**Oplossing**</span><span class="sxs-lookup"><span data-stu-id="ef9a4-109">**Resolution**</span></span>

<span data-ttu-id="ef9a4-110">Plan een automatische taak om de batchtaakgeschiedenis op te schonen.</span><span class="sxs-lookup"><span data-stu-id="ef9a4-110">Schedule an automatic task to clean up your batch job history.</span></span> <span data-ttu-id="ef9a4-111">Het is raadzaam de taak zo in te stellen dat deze wekelijks wordt uitgevoerd, maar mogelijk moet u het opschonen meer of minder vaak uitvoeren, afhankelijk van uw omgeving.</span><span class="sxs-lookup"><span data-stu-id="ef9a4-111">We recommend setting up the task to run weekly, but you might need to run the cleanup more or less frequently, depending on your environment.</span></span> <span data-ttu-id="ef9a4-112">De volgende procedure bevat de aanbevolen instellingen, maar u kunt deze wijzigen op basis van uw behoeften.</span><span class="sxs-lookup"><span data-stu-id="ef9a4-112">The following procedure contains our recommended settings, but you can change these according to your needs.</span></span>

1. <span data-ttu-id="ef9a4-113">Selecteer **Systeembeheer**in Talent.</span><span class="sxs-lookup"><span data-stu-id="ef9a4-113">In Talent, select **System administration**.</span></span>

2. <span data-ttu-id="ef9a4-114">Voer in de **Zoekbalk** de optie **Batchtaakgeschiedenis opschonen** in.</span><span class="sxs-lookup"><span data-stu-id="ef9a4-114">In the **Search** bar, enter **Batch job history clean-up**.</span></span>

   ![Zoek naar opschonen van batchtaakgeschiedenis](media/talent-batch-history-cleanup-search-bar.png)

3. <span data-ttu-id="ef9a4-116">Geef in **Geschiedenislimiet (dagen)** **30** in.</span><span class="sxs-lookup"><span data-stu-id="ef9a4-116">In **History limit (days)**, enter **30**.</span></span>

   ![Stel de geschiedenislimiet op 30](media/talent-batch-history-cleanup-history-limit.png)

4. <span data-ttu-id="ef9a4-118">Selecteer **Uitvoeren op de achtergrond** en selecteer **Terugkeerpatroon**.</span><span class="sxs-lookup"><span data-stu-id="ef9a4-118">Select **Run in the background** and then select **Recurrence**.</span></span>

   ![Stel terugkeerpatroon in](media/talent-batch-history-cleanup-recurrence.png)

5. <span data-ttu-id="ef9a4-120">Geef onder **Terugkeerpatroon definiëren** de **Begindatum** en **Begintijd** op die moeten plaatsvinden tijdens buitenuren of het weekend en selecteer vervolgens **GEEN EINDDATUM**.</span><span class="sxs-lookup"><span data-stu-id="ef9a4-120">Under **Define recurrence**, set the **Start date** and **Start time** to occur during off-hours or the weekend, and then select **NO END DATE**.</span></span> 

   ![Definieer begindatum en -tijd van het terugkeerpatroon](media/talent-batch-history-cleanup-define-recurrence.png)

6. <span data-ttu-id="ef9a4-122">Selecteer onder **TERUGKEERPATROON** **Dagen** en stel **HERHALEN NA OPGEGEVEN INTERVAL** in op **7**.</span><span class="sxs-lookup"><span data-stu-id="ef9a4-122">Under **RECURRENCE PATTERN**, select **Days** and set **REPEAT AFTER SPECIFIED INTERVAL** to **7**.</span></span>

   ![Opschonen instellen op wekelijks herhalen](media/talent-batch-history-cleanup-recurrence-pattern.png)

7. <span data-ttu-id="ef9a4-124">Selecteer **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef9a4-124">Select **OK**.</span></span>

8. <span data-ttu-id="ef9a4-125">Wijzig indien nodig andere parameters onder **Uitvoeren op de achtergrond** en selecteer vervolgens **OK**.</span><span class="sxs-lookup"><span data-stu-id="ef9a4-125">Change any other parameters under **Run in the background** as necessary, and then select **OK**.</span></span>

