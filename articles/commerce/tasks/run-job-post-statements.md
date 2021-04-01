---
title: Configureren en uitvoeren van taak om overzichten te boeken
description: Deze procedure doorloopt de configuratie en uitvoering van een terugkerende batchtaak om overzichten te boeken voor een geselecteerde winkel of groep winkels.
author: josaw1
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2b1401d51491205731843abe6e2278f798c5c979
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nl-NL
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232732"
---
# <a name="configure-and-run-job-to-post-statements"></a><span data-ttu-id="66793-103">Configureren en uitvoeren van taak om overzichten te boeken</span><span class="sxs-lookup"><span data-stu-id="66793-103">Configure and run job to post statements</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="66793-104">Deze procedure doorloopt de configuratie en uitvoering van een terugkerende batchtaak om overzichten te boeken voor een geselecteerde winkel of groep winkels.</span><span class="sxs-lookup"><span data-stu-id="66793-104">This procedure walks through configuring and running a recurrent batch job to post statements for a selected store or group of stores.</span></span> <span data-ttu-id="66793-105">Deze procedure gebruikt het demobedrijf USRT.</span><span class="sxs-lookup"><span data-stu-id="66793-105">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="66793-106">Ga naar Alle werkgebieden > ..</span><span class="sxs-lookup"><span data-stu-id="66793-106">Go to All workspaces > ..</span></span> <span data-ttu-id="66793-107">> Financiën van winkel.</span><span class="sxs-lookup"><span data-stu-id="66793-107">> Store financials.</span></span>
2. <span data-ttu-id="66793-108">Klik op Overzichten in batch boeken.</span><span class="sxs-lookup"><span data-stu-id="66793-108">Click Post statements in batch.</span></span>
    * <span data-ttu-id="66793-109">Selecteer een organisatiehiërarchie en selecteer vervolgens in de structuur van organisatieknooppunten een individuele winkel of een knooppunt.</span><span class="sxs-lookup"><span data-stu-id="66793-109">Select an organizational hierarchy and then in the organization nodes tree, select either an individual store or a node.</span></span> <span data-ttu-id="66793-110">Selecteer een knooppunt als u de batchtaak wilt maken voor een groep winkels.</span><span class="sxs-lookup"><span data-stu-id="66793-110">Select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="66793-111">Klik op de pijl om uw selectie toe te voegen.</span><span class="sxs-lookup"><span data-stu-id="66793-111">Click the arrow to add your selection.</span></span>  
3. <span data-ttu-id="66793-112">Klik op het tabblad Uitvoeren op de achtergrond. ![Uitvoeren op de achtergrond](../dev-itpro/media/runbackground.png "Op de achtergrond uitvoeren")</span><span class="sxs-lookup"><span data-stu-id="66793-112">Click the Run in the background tab. ![Run in the background](../dev-itpro/media/runbackground.png "Run in the background")</span></span> 
4. <span data-ttu-id="66793-113">Schakel het selectievakje Batchverwerking in of uit.</span><span class="sxs-lookup"><span data-stu-id="66793-113">Check or uncheck the Batch processing checkbox.</span></span>
<span data-ttu-id="66793-114">![Batchverwerking](../dev-itpro/media/batchprocessing.png "Batchverwerking en terugkeerpatroon")</span><span class="sxs-lookup"><span data-stu-id="66793-114">![Batch Processing](../dev-itpro/media/batchprocessing.png "Batch Processing & Recurrance")</span></span> 
5. <span data-ttu-id="66793-115">Klik op Terugkeerpatroon.</span><span class="sxs-lookup"><span data-stu-id="66793-115">Click Recurrence.</span></span>
6. <span data-ttu-id="66793-116">Voer een datum in het veld Startdatum in.</span><span class="sxs-lookup"><span data-stu-id="66793-116">In the Start date field, enter a date.</span></span>
7. <span data-ttu-id="66793-117">Voer een tijd in het veld Begintijd in.</span><span class="sxs-lookup"><span data-stu-id="66793-117">In the Start time field, enter a time.</span></span>
    * <span data-ttu-id="66793-118">Kies of u de herhaling wilt beëindigen na een bepaald aantal uitvoeringen, op een specifieke datum of nooit.</span><span class="sxs-lookup"><span data-stu-id="66793-118">Choose whether you want to end the recurrence after a specific number of runs, at a specific date, or never.</span></span> <span data-ttu-id="66793-119">Kies vervolgens de verschillende opties om te bepalen hoe vaak u de taak wilt uitvoeren.</span><span class="sxs-lookup"><span data-stu-id="66793-119">Then choose the various options to define how frequently you want the job to run.</span></span>  
8. <span data-ttu-id="66793-120">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="66793-120">Click OK.</span></span>
9. <span data-ttu-id="66793-121">Klik op OK.</span><span class="sxs-lookup"><span data-stu-id="66793-121">Click OK.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]